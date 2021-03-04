---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 4DCF54BA-CFFA-4555-8CA3-66B98F704EFB
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGateway.md
ms.openlocfilehash: 04026cf8cc01e1733c44821824ca4b0682b2b66d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888257"
---
# <span data-ttu-id="3d5c9-101">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="3d5c9-101">New-AzDataFactoryGateway</span></span>

## <span data-ttu-id="3d5c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d5c9-102">SYNOPSIS</span></span>
<span data-ttu-id="3d5c9-103">Cria um gateway para uma Fábrica de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="3d5c9-103">Creates a gateway for an Azure Data Factory.</span></span>

## <span data-ttu-id="3d5c9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3d5c9-104">SYNTAX</span></span>

### <span data-ttu-id="3d5c9-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3d5c9-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [[-Description] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d5c9-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="3d5c9-106">ByFactoryObject</span></span>
```
New-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [[-Description] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d5c9-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3d5c9-107">DESCRIPTION</span></span>
<span data-ttu-id="3d5c9-108">O cmdlet **New-AzDataFactoryGateway** cria um gateway no Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="3d5c9-108">The **New-AzDataFactoryGateway** cmdlet creates a gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="3d5c9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3d5c9-109">EXAMPLES</span></span>

### <span data-ttu-id="3d5c9-110">Exemplo 1: Criar um gateway</span><span class="sxs-lookup"><span data-stu-id="3d5c9-110">Example 1: Create a gateway</span></span>
```
PS C:\>New-AzDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
Name              : ContosoGateway
Description       : my gateway
Version           : 
Status            : NeedRegistration
VersionStatus     : None
CreateTime        : 8/22/2014 1:40:34 AM
RegisterTime      : 
LastConnectTime   : 
ExpiryTime        : 
ProvisioningState : Succeeded
Key               : ADF#40cbb3d9-2736-4794-a8a6-e6b839b4894f@a2d875ce-c9d7-4b8b-ad65-dd3ebbb9a940@8c0d1801-e863-44af-82e6-fb2f0c00f2ae@xz#Y9R0NhAeH3u7wgnrJyiWj4Y/QIhH4fFilIdzZgwsVQA=
```

<span data-ttu-id="3d5c9-111">Este comando cria um gateway chamado ContosoGateway no fábrica de dados chamado WikiADF no grupo de recursos chamado ADF.</span><span class="sxs-lookup"><span data-stu-id="3d5c9-111">This command creates a gateway named ContosoGateway in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="3d5c9-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3d5c9-112">PARAMETERS</span></span>

### <span data-ttu-id="3d5c9-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="3d5c9-113">-DataFactory</span></span>
<span data-ttu-id="3d5c9-114">Especifica um **objeto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="3d5c9-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="3d5c9-115">Este cmdlet cria um gateway para o fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="3d5c9-115">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d5c9-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3d5c9-116">-DataFactoryName</span></span>
<span data-ttu-id="3d5c9-117">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="3d5c9-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="3d5c9-118">Este cmdlet cria um gateway para o fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="3d5c9-118">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d5c9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d5c9-119">-DefaultProfile</span></span>
<span data-ttu-id="3d5c9-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="3d5c9-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d5c9-121">-Description</span><span class="sxs-lookup"><span data-stu-id="3d5c9-121">-Description</span></span>
<span data-ttu-id="3d5c9-122">Especifica uma descrição para o gateway.</span><span class="sxs-lookup"><span data-stu-id="3d5c9-122">Specifies a description for the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d5c9-123">-Name</span><span class="sxs-lookup"><span data-stu-id="3d5c9-123">-Name</span></span>
<span data-ttu-id="3d5c9-124">Especifica o nome do gateway a ser criado.</span><span class="sxs-lookup"><span data-stu-id="3d5c9-124">Specifies the name of the gateway to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d5c9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d5c9-125">-ResourceGroupName</span></span>
<span data-ttu-id="3d5c9-126">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="3d5c9-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="3d5c9-127">Este cmdlet cria um gateway que pertence ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="3d5c9-127">This cmdlet creates a gateway that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d5c9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d5c9-128">CommonParameters</span></span>
<span data-ttu-id="3d5c9-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d5c9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d5c9-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d5c9-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d5c9-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3d5c9-131">INPUTS</span></span>

### <span data-ttu-id="3d5c9-132">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="3d5c9-132">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="3d5c9-133">System.String</span><span class="sxs-lookup"><span data-stu-id="3d5c9-133">System.String</span></span>

## <span data-ttu-id="3d5c9-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3d5c9-134">OUTPUTS</span></span>

### <span data-ttu-id="3d5c9-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="3d5c9-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="3d5c9-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="3d5c9-136">NOTES</span></span>
* <span data-ttu-id="3d5c9-137">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="3d5c9-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3d5c9-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3d5c9-138">RELATED LINKS</span></span>

[<span data-ttu-id="3d5c9-139">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="3d5c9-139">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)

[<span data-ttu-id="3d5c9-140">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="3d5c9-140">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)


