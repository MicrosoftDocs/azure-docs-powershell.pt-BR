---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: D85FF5ED-23EA-48C7-8E61-D931713E0064
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGateway.md
ms.openlocfilehash: 6d7b82a3046b56b473140b6830a0b04333cba9b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112534"
---
# <span data-ttu-id="29a99-101">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="29a99-101">Get-AzDataFactoryGateway</span></span>

## <span data-ttu-id="29a99-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="29a99-102">SYNOPSIS</span></span>
<span data-ttu-id="29a99-103">Obtém informações sobre gateways lógicos no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="29a99-103">Gets information about logical gateways in Azure Data Factory.</span></span>

## <span data-ttu-id="29a99-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29a99-104">SYNTAX</span></span>

### <span data-ttu-id="29a99-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="29a99-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryGateway [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29a99-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="29a99-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29a99-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="29a99-107">DESCRIPTION</span></span>
<span data-ttu-id="29a99-108">O cmdlet **Get-AzDataFactoryGateway** Obtém informações sobre gateways lógicos no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="29a99-108">The **Get-AzDataFactoryGateway** cmdlet gets information about logical gateways in Azure Data Factory.</span></span>
<span data-ttu-id="29a99-109">Se você especificar o nome de um gateway, esse cmdlet obterá informações sobre esse gateway.</span><span class="sxs-lookup"><span data-stu-id="29a99-109">If you specify the name of a gateway, this cmdlet gets information about that gateway.</span></span>
<span data-ttu-id="29a99-110">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os gateways de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="29a99-110">If you do not specify a name, this cmdlet gets information about all gateways for a data factory.</span></span>
<span data-ttu-id="29a99-111">Se quiser adicionar um Microsoft SQL Server local como um serviço vinculado a uma fábrica de dados, você deve instalar um gateway em seu computador local.</span><span class="sxs-lookup"><span data-stu-id="29a99-111">If you want to add an on-premises Microsoft SQL Server as a linked service to a data factory, you must install a gateway on your on-premises computer.</span></span>

## <span data-ttu-id="29a99-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="29a99-112">EXAMPLES</span></span>

### <span data-ttu-id="29a99-113">Exemplo 1: obter todos os gateways lógicos em uma fábrica de dados</span><span class="sxs-lookup"><span data-stu-id="29a99-113">Example 1: Get all logical gateways in a data factory</span></span>
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

<span data-ttu-id="29a99-114">Esse comando obtém informações sobre todos os gateways lógicos para o data Factory chamado WikiADF no grupo de recursos chamado ADF.</span><span class="sxs-lookup"><span data-stu-id="29a99-114">This command gets information about all logical gateways for the data factory named WikiADF in the resource group named ADF.</span></span>

### <span data-ttu-id="29a99-115">Exemplo 2: obter um gateway lógico específico em uma fábrica de dados</span><span class="sxs-lookup"><span data-stu-id="29a99-115">Example 2: Get a specific logical gateway in a data factory</span></span>
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

<span data-ttu-id="29a99-116">Esse comando obtém informações sobre o gateway lógico chamado Gateway01 na fábrica de dados chamado WikiADF no grupo de recursos chamado ADF.</span><span class="sxs-lookup"><span data-stu-id="29a99-116">This command gets information about the logical gateway named Gateway01 in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="29a99-117">OS</span><span class="sxs-lookup"><span data-stu-id="29a99-117">PARAMETERS</span></span>

### <span data-ttu-id="29a99-118">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="29a99-118">-DataFactory</span></span>
<span data-ttu-id="29a99-119">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="29a99-119">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="29a99-120">Esse cmdlet obtém informações sobre os gateways lógicos na fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="29a99-120">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="29a99-121">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="29a99-121">-DataFactoryName</span></span>
<span data-ttu-id="29a99-122">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="29a99-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="29a99-123">Esse cmdlet obtém informações sobre os gateways lógicos na fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="29a99-123">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="29a99-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29a99-124">-DefaultProfile</span></span>
<span data-ttu-id="29a99-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="29a99-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29a99-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="29a99-126">-Name</span></span>
<span data-ttu-id="29a99-127">Especifica o nome do gateway lógico sobre o qual obter informações.</span><span class="sxs-lookup"><span data-stu-id="29a99-127">Specifies the name of the logical gateway about which to get information.</span></span>

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

### <span data-ttu-id="29a99-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29a99-128">-ResourceGroupName</span></span>
<span data-ttu-id="29a99-129">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="29a99-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="29a99-130">Esse cmdlet obtém informações sobre os gateways lógicos que pertencem ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="29a99-130">This cmdlet gets information about logical gateways that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="29a99-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29a99-131">CommonParameters</span></span>
<span data-ttu-id="29a99-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29a99-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29a99-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29a99-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29a99-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="29a99-134">INPUTS</span></span>

### <span data-ttu-id="29a99-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="29a99-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="29a99-136">System. String</span><span class="sxs-lookup"><span data-stu-id="29a99-136">System.String</span></span>

## <span data-ttu-id="29a99-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="29a99-137">OUTPUTS</span></span>

### <span data-ttu-id="29a99-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="29a99-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="29a99-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="29a99-139">NOTES</span></span>
* <span data-ttu-id="29a99-140">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="29a99-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="29a99-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="29a99-141">RELATED LINKS</span></span>

[<span data-ttu-id="29a99-142">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="29a99-142">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="29a99-143">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="29a99-143">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)

[<span data-ttu-id="29a99-144">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="29a99-144">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)


