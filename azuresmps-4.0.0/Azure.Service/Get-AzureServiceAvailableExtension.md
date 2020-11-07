---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BFB0000C-2EFF-4216-923B-55B0B07BFE60
online version: ''
schema: 2.0.0
ms.openlocfilehash: 51ab7d137fbbac1925ae689a1dcb16c89b9b8000
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945606"
---
# <span data-ttu-id="267e4-101">Get-AzureServiceAvailableExtension</span><span class="sxs-lookup"><span data-stu-id="267e4-101">Get-AzureServiceAvailableExtension</span></span>

## <span data-ttu-id="267e4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="267e4-102">SYNOPSIS</span></span>
<span data-ttu-id="267e4-103">Obtém informações sobre as extensões disponíveis para serviços hospedados.</span><span class="sxs-lookup"><span data-stu-id="267e4-103">Gets information about the available extensions for hosted services.</span></span>

## <span data-ttu-id="267e4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="267e4-104">SYNTAX</span></span>

### <span data-ttu-id="267e4-105">ListLatestExtensions (padrão)</span><span class="sxs-lookup"><span data-stu-id="267e4-105">ListLatestExtensions (Default)</span></span>
```
Get-AzureServiceAvailableExtension [[-ExtensionName] <String>] [[-ProviderNamespace] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="267e4-106">ListAllVersions</span><span class="sxs-lookup"><span data-stu-id="267e4-106">ListAllVersions</span></span>
```
Get-AzureServiceAvailableExtension [-ExtensionName] <String> [-ProviderNamespace] <String> [-AllVersions]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="267e4-107">ListSingleVersion</span><span class="sxs-lookup"><span data-stu-id="267e4-107">ListSingleVersion</span></span>
```
Get-AzureServiceAvailableExtension [-ExtensionName] <String> [-ProviderNamespace] <String> [-Version] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="267e4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="267e4-108">DESCRIPTION</span></span>
<span data-ttu-id="267e4-109">O cmdlet **Get-AzureServiceAvailableExtension** Obtém informações para as extensões mais recentes disponíveis para serviços hospedados.</span><span class="sxs-lookup"><span data-stu-id="267e4-109">The **Get-AzureServiceAvailableExtension** cmdlet gets information for the latest available extensions for hosted services.</span></span>

## <span data-ttu-id="267e4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="267e4-110">EXAMPLES</span></span>

### <span data-ttu-id="267e4-111">Exemplo 1: obter extensões disponíveis</span><span class="sxs-lookup"><span data-stu-id="267e4-111">Example 1: Get available extensions</span></span>
```
PS C:\> Get-AzureServiceAvailableExtension

          ProviderNameSpace          : Microsoft.Windows.Azure.Extensions
          ExtensionName              : RDP
          Version                    : 1.0
          Label                      : Microsoft Azure Remote Desktop Extension
          Description                : Microsoft Azure Remote Desktop Extension
          HostingResources           : WebOrWorkerRole
          ThumbprintAlgorithm        : sha1
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PublicConfig"><xs:complexType><xs:sequence><xs:element
          name="UserName" type="xs:string" minOccurs="1" /><xs:element name="Expiration" type="xs:string" minOccurs="1"
          /></xs:sequence></xs:complexType></xs:element></xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PrivateConfig"><xs:complexType><xs:sequence><xs:element
          name="Password" type="xs:string" /></xs:sequence></xs:complexType></xs:element></xs:schema>
          OperationDescription       : Get-AzureServiceAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="267e4-112">Este comando obtém todas as extensões disponíveis.</span><span class="sxs-lookup"><span data-stu-id="267e4-112">This command gets all available extensions.</span></span>

### <span data-ttu-id="267e4-113">Exemplo 2: obter extensões em um namespace especificado</span><span class="sxs-lookup"><span data-stu-id="267e4-113">Example 2: Get extensions in a specified namespace</span></span>
```
PS C:\> Get-AzureServiceAvailableExtension -ProviderNamespace Microsoft.Windows.Azure.Extensions -ExtensionName "RDP" -AllVersions

          ProviderNameSpace          : Microsoft.Windows.Azure.Extensions
          ExtensionName              : RDP
          Version                    : 1.0.0.1
          Label                      : Microsoft Azure Remote Desktop Extension
          Description                : Microsoft Azure Remote Desktop Extension
          HostingResources           : WebOrWorkerRole
          ThumbprintAlgorithm        : sha1
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PublicConfig"><xs:complexType><xs:sequence><xs:element
          name="UserName" type="xs:string" minOccurs="1" /><xs:element name="Expiration" type="xs:string" minOccurs="1"
          /></xs:sequence></xs:complexType></xs:element></xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PrivateConfig"><xs:complexType><xs:sequence><xs:element
          name="Password" type="xs:string" /></xs:sequence></xs:complexType></xs:element></xs:schema>
          OperationDescription       : Get-AzureServiceAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="267e4-114">Este comando obtém as extensões com um nome especificado em um namespace especificado.</span><span class="sxs-lookup"><span data-stu-id="267e4-114">This command gets the extensions with a specified name in a specified namespace.</span></span>

### <span data-ttu-id="267e4-115">Exemplo 3: obter uma versão específica de uma extensão</span><span class="sxs-lookup"><span data-stu-id="267e4-115">Example 3: Get a specific version of an extension</span></span>
```
PS C:\> Get-AzureServiceAvailableExtension -ProviderNamespace Microsoft.Windows.Azure.Extensions -ExtensionName "RDP" -Version 1.0.0.1

          ProviderNameSpace          : Microsoft.Windows.Azure.Extensions
          ExtensionName              : RDP
          Version                    : 1.0.0.1
          Label                      : Microsoft Azure Remote Desktop Extension
          Description                : Microsoft Azure Remote Desktop Extension
          HostingResources           : WebOrWorkerRole
          ThumbprintAlgorithm        : sha1
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PublicConfig"><xs:complexType><xs:sequence><xs:element
          name="UserName" type="xs:string" minOccurs="1" /><xs:element name="Expiration" type="xs:string" minOccurs="1"
          /></xs:sequence></xs:complexType></xs:element></xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PrivateConfig"><xs:complexType><xs:sequence><xs:element
          name="Password" type="xs:string" /></xs:sequence></xs:complexType></xs:element></xs:schema>
          OperationDescription       : Get-AzureServiceAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="267e4-116">Esse comando obtém informações sobre uma versão específica de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="267e4-116">This command gets information about a specific version of an extension.</span></span>

## <span data-ttu-id="267e4-117">OS</span><span class="sxs-lookup"><span data-stu-id="267e4-117">PARAMETERS</span></span>

### <span data-ttu-id="267e4-118">-Minhas versões</span><span class="sxs-lookup"><span data-stu-id="267e4-118">-AllVersions</span></span>
<span data-ttu-id="267e4-119">Indica que esse cmdlet obtém todas as versões de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="267e4-119">Indicates that this cmdlet gets all versions of an extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListAllVersions
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="267e4-120">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="267e4-120">-ExtensionName</span></span>
<span data-ttu-id="267e4-121">Especifica o nome da extensão.</span><span class="sxs-lookup"><span data-stu-id="267e4-121">Specifies the extension name.</span></span>

```yaml
Type: String
Parameter Sets: ListLatestExtensions
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ListAllVersions, ListSingleVersion
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="267e4-122">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="267e4-122">-InformationAction</span></span>
<span data-ttu-id="267e4-123">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="267e4-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="267e4-124">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="267e4-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="267e4-125">Contínuo</span><span class="sxs-lookup"><span data-stu-id="267e4-125">Continue</span></span>
- <span data-ttu-id="267e4-126">Ignorar</span><span class="sxs-lookup"><span data-stu-id="267e4-126">Ignore</span></span>
- <span data-ttu-id="267e4-127">Inquire</span><span class="sxs-lookup"><span data-stu-id="267e4-127">Inquire</span></span>
- <span data-ttu-id="267e4-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="267e4-128">SilentlyContinue</span></span>
- <span data-ttu-id="267e4-129">Finaliza</span><span class="sxs-lookup"><span data-stu-id="267e4-129">Stop</span></span>
- <span data-ttu-id="267e4-130">Suspensão</span><span class="sxs-lookup"><span data-stu-id="267e4-130">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="267e4-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="267e4-131">-InformationVariable</span></span>
<span data-ttu-id="267e4-132">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="267e4-132">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="267e4-133">-Perfil</span><span class="sxs-lookup"><span data-stu-id="267e4-133">-Profile</span></span>
<span data-ttu-id="267e4-134">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="267e4-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="267e4-135">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="267e4-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="267e4-136">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="267e4-136">-ProviderNamespace</span></span>
<span data-ttu-id="267e4-137">Especifica o namespace do provedor de extensão.</span><span class="sxs-lookup"><span data-stu-id="267e4-137">Specifies the extension provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: ListLatestExtensions
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ListAllVersions, ListSingleVersion
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="267e4-138">-Versão</span><span class="sxs-lookup"><span data-stu-id="267e4-138">-Version</span></span>
<span data-ttu-id="267e4-139">Especifica a versão de extensão.</span><span class="sxs-lookup"><span data-stu-id="267e4-139">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: ListSingleVersion
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="267e4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="267e4-140">CommonParameters</span></span>
<span data-ttu-id="267e4-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="267e4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="267e4-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="267e4-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="267e4-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="267e4-143">INPUTS</span></span>

## <span data-ttu-id="267e4-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="267e4-144">OUTPUTS</span></span>

## <span data-ttu-id="267e4-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="267e4-145">NOTES</span></span>

## <span data-ttu-id="267e4-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="267e4-146">RELATED LINKS</span></span>

[<span data-ttu-id="267e4-147">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="267e4-147">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)


