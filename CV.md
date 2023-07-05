# Gorchanin Dmitriy
<img src="image.png" alt="Photo" width="275"/>

## How to contact me
* Mobile phone: +375 44 xxx xx-73
* E-mail: dmitriygorchanin@gmail.com
* [Telegram](https://t.me/Gh0st_Fighter)
* [LinkedIn](https://www.linkedin.com/in/d-gorchanin/)
* [VK](https://vk.com/d.gorchanin)

## About me
I am second graduate student in Belarusian-Russian university with huge willing to learn and work. I do not have any experience in work with production code, but I have worked on many small projects. Now I am working on one big personal project in the team of 4 groupmates. I have a good knowledge of C# and understanding OOP and SOLID principles, have experience in work with MS SQL Server. Also I have a little experience in work with API (ASP.NET) with using REST architecture.

## Skills
### Hard skills
* C#
* .NET
* SQL
* JavaScript
* HTML/CSS
* Python
* Figma
### Soft skills
* Puncuality
* Responsibility
* Altruism
### English Level
Upper-Intermediate (B2)

## Code Example

    namespace Model.Serialization
    {
        [AttributeUsage(AttributeTargets.Class | AttributeTargets.Struct)]
        public class JsonIncludePrivateFieldsAttribute : Attribute { }

        public static class PrivateFieldSerialize
        {
            public static void AddPrivateFieldsModifier(JsonTypeInfo jsonTypeInfo)
            {
                if (jsonTypeInfo.Kind != JsonTypeInfoKind.Object)
                    return;
                if (!jsonTypeInfo.Type.IsDefined(typeof (JsonIncludePrivateFieldsAttribute), inherit: false))
                    return;

                foreach (FieldInfo field in jsonTypeInfo.Type.GetFields(BindingFlags.Instance | BindingFlags.NonPublic))
                {
                    JsonPropertyInfo jsonPropertyInfo = jsonTypeInfo.CreateJsonPropertyInfo(field.FieldType, field.Name);
                    jsonPropertyInfo.Get = field.GetValue;
                    jsonPropertyInfo.Set = field.SetValue;

                    jsonTypeInfo.Properties.Add(jsonPropertyInfo);
                }
            }
        }
    }

## Completed Trainings
### .NET Development
EPAM training center 

01/2022-05/2022

## Projects
### Project Enrollee

This program targets to fractionally simplify the proccess of documents submission in university.

Technologies: JavaScript, Bootstrap, C#, ASP.NET, Microsoft Office Interop
### Document Scanner 

This program scans passport or it alternatives and shows all neccessary data about it handler

Technologies: C#, IronOCR library
### (In progress) Personal computer hardware configurator

This web-application helps user in personal computer hardware's selection. It checks components' compatibility and divides issues into two levels: major and warning

Technologies: React, NodeJS, PostgreSQL
