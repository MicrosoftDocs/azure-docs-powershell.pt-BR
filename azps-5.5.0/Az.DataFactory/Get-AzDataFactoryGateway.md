---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: D85FF5ED-23EA-48C7-8E61-D931713E0064
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGateway.md
ms.openlocfilehash: 6d7b82a3046b56b473140b6830a0b04333cba9b0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116440"
---
# <span data-ttu-id="9f005-101">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9f005-101">Get-AzDataFactoryGateway</span></span>

## <span data-ttu-id="9f005-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9f005-102">SYNOPSIS</span></span>
<span data-ttu-id="9f005-103">Obtém informações sobre gateways lógicos no Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="9f005-103">Gets information about logical gateways in Azure Data Factory.</span></span>

## <span data-ttu-id="9f005-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f005-104">SYNTAX</span></span>

### <span data-ttu-id="9f005-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="9f005-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryGateway [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f005-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9f005-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f005-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="9f005-107">DESCRIPTION</span></span>
<span data-ttu-id="9f005-108">O cmdlet **Get-AzDataFactoryGateway** obtém informações sobre gateways lógicos no Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="9f005-108">The **Get-AzDataFactoryGateway** cmdlet gets information about logical gateways in Azure Data Factory.</span></span>
<span data-ttu-id="9f005-109">Se você especificar o nome de um gateway, esse cmdlet obterá informações sobre esse gateway.</span><span class="sxs-lookup"><span data-stu-id="9f005-109">If you specify the name of a gateway, this cmdlet gets information about that gateway.</span></span>
<span data-ttu-id="9f005-110">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os gateways de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="9f005-110">If you do not specify a name, this cmdlet gets information about all gateways for a data factory.</span></span>
<span data-ttu-id="9f005-111">Se você quiser adicionar um Microsoft SQL Server local como um serviço vinculado a uma fábrica de dados, deverá instalar um gateway em seu computador local.</span><span class="sxs-lookup"><span data-stu-id="9f005-111">If you want to add an on-premises Microsoft SQL Server as a linked service to a data factory, you must install a gateway on your on-premises computer.</span></span>

## <span data-ttu-id="9f005-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9f005-112">EXAMPLES</span></span>

### <span data-ttu-id="9f005-113">Exemplo 1: Obter todos os gateways lógicos em uma fábrica de dados</span><span class="sxs-lookup"><span data-stu-id="9f005-113">Example 1: Get all logical gateways in a data factory</span></span>
```
PS C:\>Get-AzDataFactoryGateway -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
Name            : gateway1
Description     : 
Version         : 1.3.5338.1
Status          : Online
VersionStatus   : UpToDate
CreateTime      : 8/22/2014 1:40:34 AM
RegisterTime    : 8/22/2014 1:41:46 AM
LastConnectTime : 8/22/2014 1:44:56 AM
ExpiryTime      : 
Name            : gateway2
Description     : 
Version         : 1.3.5338.1
Status          : Offline
VersionStatus   : UpToDate
CreateTime      : 8/29/2014 1:46:44 AM
RegisterTime    : 8/29/2014 1:48:36 AM
LastConnectTime : 8/29/2014 1:56:56 AM
ExpiryTime      :
```

<span data-ttu-id="9f005-114">Esse comando obtém informações sobre todos os gateways lógicos para o fábrica de dados chamado WikiADF no grupo de recursos chamado ADF.</span><span class="sxs-lookup"><span data-stu-id="9f005-114">This command gets information about all logical gateways for the data factory named WikiADF in the resource group named ADF.</span></span>

### <span data-ttu-id="9f005-115">Exemplo 2: Obter um gateway lógico específico em uma fábrica de dados</span><span class="sxs-lookup"><span data-stu-id="9f005-115">Example 2: Get a specific logical gateway in a data factory</span></span>
```
PS C:\>Get-AzDataFactoryGateway -ResourceGroupName "ADF" -Name "Gateway01" -DataFactoryName "WikiADF"
Name            : Gateway01
Description     : 
Version         : 1.3.5338.1
Status          : Online
VersionStatus   : UpToDate
CreateTime      : 8/22/2014 1:40:34 AM
RegisterTime    : 8/22/2014 1:41:46 AM
LastConnectTime : 8/22/2014 1:44:56 AM
ExpiryTime      :
```

<span data-ttu-id="9f005-116">Esse comando obtém informações sobre o gateway lógico chamado Gateway01 na fábrica de dados chamada WikiADF no grupo de recursos chamado ADF.</span><span class="sxs-lookup"><span data-stu-id="9f005-116">This command gets information about the logical gateway named Gateway01 in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="9f005-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f005-117">PARAMETERS</span></span>

### <span data-ttu-id="9f005-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="9f005-118">-DataFactory</span></span>
<span data-ttu-id="9f005-119">Especifica um **objeto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="9f005-119">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="9f005-120">Este cmdlet obtém informações sobre gateways lógicos no fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="9f005-120">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9f005-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9f005-121">-DataFactoryName</span></span>
<span data-ttu-id="9f005-122">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="9f005-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="9f005-123">Este cmdlet obtém informações sobre gateways lógicos no fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="9f005-123">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9f005-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f005-124">-DefaultProfile</span></span>
<span data-ttu-id="9f005-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="9f005-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f005-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="9f005-126">-Name</span></span>
<span data-ttu-id="9f005-127">Especifica o nome do gateway lógico sobre o qual obter informações.</span><span class="sxs-lookup"><span data-stu-id="9f005-127">Specifies the name of the logical gateway about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f005-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f005-128">-ResourceGroupName</span></span>
<span data-ttu-id="9f005-129">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="9f005-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="9f005-130">Este cmdlet obtém informações sobre gateways lógicos que pertencem ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="9f005-130">This cmdlet gets information about logical gateways that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9f005-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f005-131">CommonParameters</span></span>
<span data-ttu-id="9f005-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f005-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f005-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f005-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f005-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="9f005-134">INPUTS</span></span>

### <span data-ttu-id="9f005-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="9f005-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="9f005-136">System.String</span><span class="sxs-lookup"><span data-stu-id="9f005-136">System.String</span></span>

## <span data-ttu-id="9f005-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="9f005-137">OUTPUTS</span></span>

### <span data-ttu-id="9f005-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9f005-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="9f005-139">Notas</span><span class="sxs-lookup"><span data-stu-id="9f005-139">NOTES</span></span>
* <span data-ttu-id="9f005-140">Palavras-chave: azure, azurerm, arm, resource, management, manager, data,</span><span class="sxs-lookup"><span data-stu-id="9f005-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="9f005-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f005-141">RELATED LINKS</span></span>

[<span data-ttu-id="9f005-142">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9f005-142">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="9f005-143">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9f005-143">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)

[<span data-ttu-id="9f005-144">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9f005-144">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)


