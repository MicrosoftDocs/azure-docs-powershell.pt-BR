---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 4DCF54BA-CFFA-4555-8CA3-66B98F704EFB
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGateway.md
ms.openlocfilehash: a4c755ab3f68eab2821807e7df6b9e24fad0df9d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778338"
---
# <span data-ttu-id="a0ab5-101">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="a0ab5-101">New-AzDataFactoryGateway</span></span>

## <span data-ttu-id="a0ab5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a0ab5-102">SYNOPSIS</span></span>
<span data-ttu-id="a0ab5-103">Cria um gateway para uma fábrica de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="a0ab5-103">Creates a gateway for an Azure Data Factory.</span></span>

## <span data-ttu-id="a0ab5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0ab5-104">SYNTAX</span></span>

### <span data-ttu-id="a0ab5-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="a0ab5-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [[-Description] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0ab5-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a0ab5-106">ByFactoryObject</span></span>
```
New-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [[-Description] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0ab5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a0ab5-107">DESCRIPTION</span></span>
<span data-ttu-id="a0ab5-108">O cmdlet **New-AzDataFactoryGateway** cria um gateway no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="a0ab5-108">The **New-AzDataFactoryGateway** cmdlet creates a gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="a0ab5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a0ab5-109">EXAMPLES</span></span>

### <span data-ttu-id="a0ab5-110">Exemplo 1: criar um gateway</span><span class="sxs-lookup"><span data-stu-id="a0ab5-110">Example 1: Create a gateway</span></span>
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

<span data-ttu-id="a0ab5-111">Esse comando cria um gateway chamado ContosoGateway na fábrica de dados chamado WikiADF no grupo de recursos chamado ADF.</span><span class="sxs-lookup"><span data-stu-id="a0ab5-111">This command creates a gateway named ContosoGateway in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="a0ab5-112">OS</span><span class="sxs-lookup"><span data-stu-id="a0ab5-112">PARAMETERS</span></span>

### <span data-ttu-id="a0ab5-113">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="a0ab5-113">-DataFactory</span></span>
<span data-ttu-id="a0ab5-114">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="a0ab5-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="a0ab5-115">Esse cmdlet cria um gateway para a fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="a0ab5-115">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a0ab5-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="a0ab5-116">-DataFactoryName</span></span>
<span data-ttu-id="a0ab5-117">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="a0ab5-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="a0ab5-118">Esse cmdlet cria um gateway para a fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="a0ab5-118">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a0ab5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0ab5-119">-DefaultProfile</span></span>
<span data-ttu-id="a0ab5-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a0ab5-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0ab5-121">-Descrição</span><span class="sxs-lookup"><span data-stu-id="a0ab5-121">-Description</span></span>
<span data-ttu-id="a0ab5-122">Especifica uma descrição para o gateway.</span><span class="sxs-lookup"><span data-stu-id="a0ab5-122">Specifies a description for the gateway.</span></span>

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

### <span data-ttu-id="a0ab5-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="a0ab5-123">-Name</span></span>
<span data-ttu-id="a0ab5-124">Especifica o nome do gateway a ser criado.</span><span class="sxs-lookup"><span data-stu-id="a0ab5-124">Specifies the name of the gateway to create.</span></span>

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

### <span data-ttu-id="a0ab5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0ab5-125">-ResourceGroupName</span></span>
<span data-ttu-id="a0ab5-126">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="a0ab5-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a0ab5-127">Esse cmdlet cria um gateway que pertence ao grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="a0ab5-127">This cmdlet creates a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a0ab5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0ab5-128">CommonParameters</span></span>
<span data-ttu-id="a0ab5-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0ab5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0ab5-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0ab5-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0ab5-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a0ab5-131">INPUTS</span></span>

### <span data-ttu-id="a0ab5-132">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a0ab5-132">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="a0ab5-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a0ab5-133">System.String</span></span>

## <span data-ttu-id="a0ab5-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a0ab5-134">OUTPUTS</span></span>

### <span data-ttu-id="a0ab5-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="a0ab5-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="a0ab5-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a0ab5-136">NOTES</span></span>
* <span data-ttu-id="a0ab5-137">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="a0ab5-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a0ab5-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a0ab5-138">RELATED LINKS</span></span>

[<span data-ttu-id="a0ab5-139">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="a0ab5-139">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)

[<span data-ttu-id="a0ab5-140">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="a0ab5-140">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)


