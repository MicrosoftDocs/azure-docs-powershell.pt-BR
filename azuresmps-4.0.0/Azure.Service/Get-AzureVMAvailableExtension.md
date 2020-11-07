---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FAC3DABB-8230-4E86-9936-0F1848980EA2
online version: ''
schema: 2.0.0
ms.openlocfilehash: d062b4300af2efbd45bfccd7ed467871b23d8256
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946544"
---
# <span data-ttu-id="4fbde-101">Get-AzureVMAvailableExtension</span><span class="sxs-lookup"><span data-stu-id="4fbde-101">Get-AzureVMAvailableExtension</span></span>

## <span data-ttu-id="4fbde-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4fbde-102">SYNOPSIS</span></span>
<span data-ttu-id="4fbde-103">Obtém informações para as extensões mais recentes disponíveis para máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="4fbde-103">Gets information for the latest available extensions for virtual machines.</span></span>

## <span data-ttu-id="4fbde-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4fbde-104">SYNTAX</span></span>

### <span data-ttu-id="4fbde-105">ListLatestExtensions (padrão)</span><span class="sxs-lookup"><span data-stu-id="4fbde-105">ListLatestExtensions (Default)</span></span>
```
Get-AzureVMAvailableExtension [[-ExtensionName] <String>] [[-Publisher] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="4fbde-106">ListAllVersions</span><span class="sxs-lookup"><span data-stu-id="4fbde-106">ListAllVersions</span></span>
```
Get-AzureVMAvailableExtension [-ExtensionName] <String> [-Publisher] <String> [-AllVersions]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="4fbde-107">ListSingleVersion</span><span class="sxs-lookup"><span data-stu-id="4fbde-107">ListSingleVersion</span></span>
```
Get-AzureVMAvailableExtension [-ExtensionName] <String> [-Publisher] <String> [-Version] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="4fbde-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4fbde-108">DESCRIPTION</span></span>
<span data-ttu-id="4fbde-109">O cmdlet **Get-AzureVMAvailableExtension** Obtém informações para as extensões mais recentes disponíveis para máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="4fbde-109">The **Get-AzureVMAvailableExtension** cmdlet gets information for the latest available extensions for virtual machines.</span></span>

## <span data-ttu-id="4fbde-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4fbde-110">EXAMPLES</span></span>

### <span data-ttu-id="4fbde-111">Exemplo 1: obter informações para as extensões mais recentes disponíveis</span><span class="sxs-lookup"><span data-stu-id="4fbde-111">Example 1: Get information for the latest available extensions</span></span>
```
PS C:\> Get-AzureVMAvailableExtension
          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="4fbde-112">Esse comando obtém informações para as extensões mais recentes disponíveis para todas as máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="4fbde-112">This command gets information for the latest available extensions for all virtual machines.</span></span>

### <span data-ttu-id="4fbde-113">Exemplo 2: obter informações a partir de um nome de extensão especificado</span><span class="sxs-lookup"><span data-stu-id="4fbde-113">Example 2: Get information from a specified extension name</span></span>
```
PS C:\> Get-AzureVMAvailableExtension -Publisher Microsoft.Compute -ExtensionName "VMAccessAgent" -AllVersions
          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0.2
          PublicConfigurationSchema  : 
          <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>

          PrivateConfigurationSchema : 
          <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>

          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded

          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0.3
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="4fbde-114">Esse comando obtém informações de todas as versões da extensão chamada VMAccessAgent e o editor chamado Microsoft. Computer.</span><span class="sxs-lookup"><span data-stu-id="4fbde-114">This command gets information from all versions of the extension named VMAccessAgent and the publisher named Microsoft.Computer.</span></span>

### <span data-ttu-id="4fbde-115">Exemplo 3: obter informações de uma extensão de máquina virtual específica por número de versão</span><span class="sxs-lookup"><span data-stu-id="4fbde-115">Example 3: Get information from a specific virtual machine extension by version number</span></span>
```
PS C:\> Get-AzureVMAvailableExtension -Publisher Microsoft.Compute -ExtensionName VMAccessAgent -Version 1.0.3
          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0.3
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="4fbde-116">Esse comando obtém informações para a extensão chamada VMAccessAgent e o editor chamado Microsoft. COMPUTE para a versão de extensão 1.0.3.</span><span class="sxs-lookup"><span data-stu-id="4fbde-116">This command gets information for the extension named VMAccessAgent and the publisher named Microsoft.Compute for the extension version 1.0.3.</span></span>

## <span data-ttu-id="4fbde-117">OS</span><span class="sxs-lookup"><span data-stu-id="4fbde-117">PARAMETERS</span></span>

### <span data-ttu-id="4fbde-118">-Minhas versões</span><span class="sxs-lookup"><span data-stu-id="4fbde-118">-AllVersions</span></span>
<span data-ttu-id="4fbde-119">Indica que esse cmdlet lista todas as versões de uma extensão.</span><span class="sxs-lookup"><span data-stu-id="4fbde-119">Indicates that this cmdlet lists all versions of an extension.</span></span>

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

### <span data-ttu-id="4fbde-120">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="4fbde-120">-ExtensionName</span></span>
<span data-ttu-id="4fbde-121">Especifica o nome da extensão disponível.</span><span class="sxs-lookup"><span data-stu-id="4fbde-121">Specifies the name of the available extension.</span></span>

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

### <span data-ttu-id="4fbde-122">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="4fbde-122">-InformationAction</span></span>
<span data-ttu-id="4fbde-123">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="4fbde-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4fbde-124">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4fbde-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4fbde-125">Contínuo</span><span class="sxs-lookup"><span data-stu-id="4fbde-125">Continue</span></span>
- <span data-ttu-id="4fbde-126">Ignorar</span><span class="sxs-lookup"><span data-stu-id="4fbde-126">Ignore</span></span>
- <span data-ttu-id="4fbde-127">Inquire</span><span class="sxs-lookup"><span data-stu-id="4fbde-127">Inquire</span></span>
- <span data-ttu-id="4fbde-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4fbde-128">SilentlyContinue</span></span>
- <span data-ttu-id="4fbde-129">Finaliza</span><span class="sxs-lookup"><span data-stu-id="4fbde-129">Stop</span></span>
- <span data-ttu-id="4fbde-130">Suspensão</span><span class="sxs-lookup"><span data-stu-id="4fbde-130">Suspend</span></span>

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

### <span data-ttu-id="4fbde-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4fbde-131">-InformationVariable</span></span>
<span data-ttu-id="4fbde-132">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="4fbde-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4fbde-133">-Perfil</span><span class="sxs-lookup"><span data-stu-id="4fbde-133">-Profile</span></span>
<span data-ttu-id="4fbde-134">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="4fbde-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4fbde-135">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="4fbde-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4fbde-136">-Publisher</span><span class="sxs-lookup"><span data-stu-id="4fbde-136">-Publisher</span></span>
<span data-ttu-id="4fbde-137">Especifica o fornecedor da extensão.</span><span class="sxs-lookup"><span data-stu-id="4fbde-137">Specifies the publisher of the extension.</span></span>

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

### <span data-ttu-id="4fbde-138">-Versão</span><span class="sxs-lookup"><span data-stu-id="4fbde-138">-Version</span></span>
<span data-ttu-id="4fbde-139">Especifica a versão da extensão.</span><span class="sxs-lookup"><span data-stu-id="4fbde-139">Specifies the version of the extension.</span></span>

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

### <span data-ttu-id="4fbde-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fbde-140">CommonParameters</span></span>
<span data-ttu-id="4fbde-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fbde-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fbde-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fbde-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fbde-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4fbde-143">INPUTS</span></span>

## <span data-ttu-id="4fbde-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4fbde-144">OUTPUTS</span></span>

## <span data-ttu-id="4fbde-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4fbde-145">NOTES</span></span>

## <span data-ttu-id="4fbde-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4fbde-146">RELATED LINKS</span></span>

