---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: D85FF5ED-23EA-48C7-8E61-D931713E0064
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGateway.md
ms.openlocfilehash: 80ff3a13014bcdc05191bcf5555abf2e029a831d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888316"
---
# <span data-ttu-id="df962-101">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="df962-101">Get-AzDataFactoryGateway</span></span>

## <span data-ttu-id="df962-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df962-102">SYNOPSIS</span></span>
<span data-ttu-id="df962-103">Obtém informações sobre gateways lógicos no Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="df962-103">Gets information about logical gateways in Azure Data Factory.</span></span>

## <span data-ttu-id="df962-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="df962-104">SYNTAX</span></span>

### <span data-ttu-id="df962-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="df962-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryGateway [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df962-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="df962-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df962-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="df962-107">DESCRIPTION</span></span>
<span data-ttu-id="df962-108">O cmdlet **Get-AzDataFactoryGateway** obtém informações sobre gateways lógicos no Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="df962-108">The **Get-AzDataFactoryGateway** cmdlet gets information about logical gateways in Azure Data Factory.</span></span>
<span data-ttu-id="df962-109">Se você especificar o nome de um gateway, esse cmdlet obterá informações sobre esse gateway.</span><span class="sxs-lookup"><span data-stu-id="df962-109">If you specify the name of a gateway, this cmdlet gets information about that gateway.</span></span>
<span data-ttu-id="df962-110">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os gateways de um fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="df962-110">If you do not specify a name, this cmdlet gets information about all gateways for a data factory.</span></span>
<span data-ttu-id="df962-111">Se você quiser adicionar um serviço Microsoft SQL Server local como um serviço vinculado a um fábrica de dados, instale um gateway em seu computador local.</span><span class="sxs-lookup"><span data-stu-id="df962-111">If you want to add an on-premises Microsoft SQL Server as a linked service to a data factory, you must install a gateway on your on-premises computer.</span></span>

## <span data-ttu-id="df962-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="df962-112">EXAMPLES</span></span>

### <span data-ttu-id="df962-113">Exemplo 1: Obter todos os gateways lógicos em um fábrica de dados</span><span class="sxs-lookup"><span data-stu-id="df962-113">Example 1: Get all logical gateways in a data factory</span></span>
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

<span data-ttu-id="df962-114">Este comando obtém informações sobre todos os gateways lógicos para o fábrica de dados chamado WikiADF no grupo de recursos chamado ADF.</span><span class="sxs-lookup"><span data-stu-id="df962-114">This command gets information about all logical gateways for the data factory named WikiADF in the resource group named ADF.</span></span>

### <span data-ttu-id="df962-115">Exemplo 2: Obter um gateway lógico específico em um fábrica de dados</span><span class="sxs-lookup"><span data-stu-id="df962-115">Example 2: Get a specific logical gateway in a data factory</span></span>
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

<span data-ttu-id="df962-116">Este comando obtém informações sobre o gateway lógico chamado Gateway01 no fábrica de dados chamado WikiADF no grupo de recursos chamado ADF.</span><span class="sxs-lookup"><span data-stu-id="df962-116">This command gets information about the logical gateway named Gateway01 in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="df962-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="df962-117">PARAMETERS</span></span>

### <span data-ttu-id="df962-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="df962-118">-DataFactory</span></span>
<span data-ttu-id="df962-119">Especifica um **objeto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="df962-119">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="df962-120">Este cmdlet obtém informações sobre gateways lógicos no fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="df962-120">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="df962-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="df962-121">-DataFactoryName</span></span>
<span data-ttu-id="df962-122">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="df962-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="df962-123">Este cmdlet obtém informações sobre gateways lógicos no fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="df962-123">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="df962-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df962-124">-DefaultProfile</span></span>
<span data-ttu-id="df962-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="df962-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df962-126">-Name</span><span class="sxs-lookup"><span data-stu-id="df962-126">-Name</span></span>
<span data-ttu-id="df962-127">Especifica o nome do gateway lógico sobre o qual obter informações.</span><span class="sxs-lookup"><span data-stu-id="df962-127">Specifies the name of the logical gateway about which to get information.</span></span>

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

### <span data-ttu-id="df962-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df962-128">-ResourceGroupName</span></span>
<span data-ttu-id="df962-129">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="df962-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="df962-130">Este cmdlet obtém informações sobre gateways lógicos que pertencem ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="df962-130">This cmdlet gets information about logical gateways that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="df962-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df962-131">CommonParameters</span></span>
<span data-ttu-id="df962-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df962-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df962-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df962-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df962-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="df962-134">INPUTS</span></span>

### <span data-ttu-id="df962-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="df962-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="df962-136">System.String</span><span class="sxs-lookup"><span data-stu-id="df962-136">System.String</span></span>

## <span data-ttu-id="df962-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="df962-137">OUTPUTS</span></span>

### <span data-ttu-id="df962-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="df962-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="df962-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="df962-139">NOTES</span></span>
* <span data-ttu-id="df962-140">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="df962-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="df962-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df962-141">RELATED LINKS</span></span>

[<span data-ttu-id="df962-142">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="df962-142">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="df962-143">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="df962-143">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)

[<span data-ttu-id="df962-144">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="df962-144">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)


