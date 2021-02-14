---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 663D27A3-0B51-48F5-81D0-8DDBC5A3A33C
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryGateway.md
ms.openlocfilehash: b9eebe26e64e9a7ce2497cdf9984ca6dabb062e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111004"
---
# <span data-ttu-id="9e06d-101">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9e06d-101">Set-AzDataFactoryGateway</span></span>

## <span data-ttu-id="9e06d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9e06d-102">SYNOPSIS</span></span>
<span data-ttu-id="9e06d-103">Define a descrição de um gateway no Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="9e06d-103">Sets the description for a gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="9e06d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9e06d-104">SYNTAX</span></span>

### <span data-ttu-id="9e06d-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="9e06d-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Description] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e06d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9e06d-106">ByFactoryObject</span></span>
```
Set-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e06d-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="9e06d-107">DESCRIPTION</span></span>
<span data-ttu-id="9e06d-108">O cmdlet **Set-AzDataFactoryGateway** define a descrição do gateway especificado no Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="9e06d-108">The **Set-AzDataFactoryGateway** cmdlet sets the description for the specified gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="9e06d-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9e06d-109">EXAMPLES</span></span>

### <span data-ttu-id="9e06d-110">Exemplo 1: Definir a descrição de um gateway</span><span class="sxs-lookup"><span data-stu-id="9e06d-110">Example 1: Set the description for a gateway</span></span>
```
PS C:\>Set-AzDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
Name            : ContosoGateway
Description     : my gateway
Version         : 1.3.5338.1
Status          : Online
VersionStatus   : UpToDate
CreateTime      : 8/22/2014 1:31:09 AM
RegisterTime    : 8/22/2014 1:31:37 AM
LastConnectTime : 8/22/2014 1:41:41 AM
ExpiryTime      :
```

<span data-ttu-id="9e06d-111">Esse comando define a descrição do gateway chamado ContosoGateway na fábrica de dados chamada WikiADF.</span><span class="sxs-lookup"><span data-stu-id="9e06d-111">This command sets the description for the gateway named ContosoGateway in the data factory named WikiADF.</span></span>
<span data-ttu-id="9e06d-112">O parâmetro Descrição especifica a nova descrição.</span><span class="sxs-lookup"><span data-stu-id="9e06d-112">The Description parameter specifies the new description.</span></span>

## <span data-ttu-id="9e06d-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9e06d-113">PARAMETERS</span></span>

### <span data-ttu-id="9e06d-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="9e06d-114">-DataFactory</span></span>
<span data-ttu-id="9e06d-115">Especifica um **objeto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="9e06d-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="9e06d-116">Este cmdlet define a descrição do gateway no fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="9e06d-116">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9e06d-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9e06d-117">-DataFactoryName</span></span>
<span data-ttu-id="9e06d-118">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="9e06d-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="9e06d-119">Este cmdlet define a descrição do gateway no fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="9e06d-119">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9e06d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e06d-120">-DefaultProfile</span></span>
<span data-ttu-id="9e06d-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="9e06d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e06d-122">-Descrição</span><span class="sxs-lookup"><span data-stu-id="9e06d-122">-Description</span></span>
<span data-ttu-id="9e06d-123">Especifica uma descrição para o gateway.</span><span class="sxs-lookup"><span data-stu-id="9e06d-123">Specifies a description for the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e06d-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="9e06d-124">-Name</span></span>
<span data-ttu-id="9e06d-125">Especifica o nome do gateway para o qual definir uma descrição.</span><span class="sxs-lookup"><span data-stu-id="9e06d-125">Specifies the name of the gateway for which to set a description.</span></span>

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

### <span data-ttu-id="9e06d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e06d-126">-ResourceGroupName</span></span>
<span data-ttu-id="9e06d-127">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="9e06d-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="9e06d-128">Esse cmdlet define a descrição de um gateway que pertence ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="9e06d-128">This cmdlet sets the description for a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9e06d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e06d-129">CommonParameters</span></span>
<span data-ttu-id="9e06d-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e06d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e06d-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e06d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e06d-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="9e06d-132">INPUTS</span></span>

### <span data-ttu-id="9e06d-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="9e06d-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="9e06d-134">System.String</span><span class="sxs-lookup"><span data-stu-id="9e06d-134">System.String</span></span>

## <span data-ttu-id="9e06d-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="9e06d-135">OUTPUTS</span></span>

### <span data-ttu-id="9e06d-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9e06d-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="9e06d-137">Notas</span><span class="sxs-lookup"><span data-stu-id="9e06d-137">NOTES</span></span>
* <span data-ttu-id="9e06d-138">Palavras-chave: azure, azurerm, arm, resource, management, manager, data,</span><span class="sxs-lookup"><span data-stu-id="9e06d-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="9e06d-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9e06d-139">RELATED LINKS</span></span>

[<span data-ttu-id="9e06d-140">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9e06d-140">Get-AzDataFactoryGateway</span></span>](./Get-AzDataFactoryGateway.md)

[<span data-ttu-id="9e06d-141">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9e06d-141">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="9e06d-142">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9e06d-142">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)


