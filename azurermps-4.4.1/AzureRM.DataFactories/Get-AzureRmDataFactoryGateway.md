---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: D85FF5ED-23EA-48C7-8E61-D931713E0064
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryGateway.md
ms.openlocfilehash: a90146480b0706d88f4ef7626b83008e08c22232
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610826"
---
# <span data-ttu-id="1b857-101">Get-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="1b857-101">Get-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="1b857-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1b857-102">SYNOPSIS</span></span>
<span data-ttu-id="1b857-103">Obtém informações sobre gateways lógicos no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="1b857-103">Gets information about logical gateways in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b857-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1b857-104">SYNTAX</span></span>

### <span data-ttu-id="1b857-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="1b857-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryGateway [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b857-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1b857-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b857-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1b857-107">DESCRIPTION</span></span>
<span data-ttu-id="1b857-108">O cmdlet **Get-AzureRmDataFactoryGateway** Obtém informações sobre gateways lógicos no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="1b857-108">The **Get-AzureRmDataFactoryGateway** cmdlet gets information about logical gateways in Azure Data Factory.</span></span>
<span data-ttu-id="1b857-109">Se você especificar o nome de um gateway, esse cmdlet obterá informações sobre esse gateway.</span><span class="sxs-lookup"><span data-stu-id="1b857-109">If you specify the name of a gateway, this cmdlet gets information about that gateway.</span></span>
<span data-ttu-id="1b857-110">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os gateways de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="1b857-110">If you do not specify a name, this cmdlet gets information about all gateways for a data factory.</span></span>

<span data-ttu-id="1b857-111">Se quiser adicionar um Microsoft SQL Server local como um serviço vinculado a uma fábrica de dados, você deve instalar um gateway em seu computador local.</span><span class="sxs-lookup"><span data-stu-id="1b857-111">If you want to add an on-premises Microsoft SQL Server as a linked service to a data factory, you must install a gateway on your on-premises computer.</span></span>

## <span data-ttu-id="1b857-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1b857-112">EXAMPLES</span></span>

### <span data-ttu-id="1b857-113">Exemplo 1: obter todos os gateways lógicos em uma fábrica de dados</span><span class="sxs-lookup"><span data-stu-id="1b857-113">Example 1: Get all logical gateways in a data factory</span></span>
```
PS C:\>Get-AzureRmDataFactoryGateway -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
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

<span data-ttu-id="1b857-114">Esse comando obtém informações sobre todos os gateways lógicos para o data Factory chamado WikiADF no grupo de recursos chamado ADF.</span><span class="sxs-lookup"><span data-stu-id="1b857-114">This command gets information about all logical gateways for the data factory named WikiADF in the resource group named ADF.</span></span>

### <span data-ttu-id="1b857-115">Exemplo 2: obter um gateway lógico específico em uma fábrica de dados</span><span class="sxs-lookup"><span data-stu-id="1b857-115">Example 2: Get a specific logical gateway in a data factory</span></span>
```
PS C:\>Get-AzureRmDataFactoryGateway -ResourceGroupName "ADF" -Name "Gateway01" -DataFactoryName "WikiADF"
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

<span data-ttu-id="1b857-116">Esse comando obtém informações sobre o gateway lógico chamado Gateway01 na fábrica de dados chamado WikiADF no grupo de recursos chamado ADF.</span><span class="sxs-lookup"><span data-stu-id="1b857-116">This command gets information about the logical gateway named Gateway01 in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="1b857-117">OS</span><span class="sxs-lookup"><span data-stu-id="1b857-117">PARAMETERS</span></span>

### <span data-ttu-id="1b857-118">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="1b857-118">-DataFactory</span></span>
<span data-ttu-id="1b857-119">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="1b857-119">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="1b857-120">Esse cmdlet obtém informações sobre os gateways lógicos na fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="1b857-120">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1b857-121">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="1b857-121">-DataFactoryName</span></span>
<span data-ttu-id="1b857-122">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="1b857-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="1b857-123">Esse cmdlet obtém informações sobre os gateways lógicos na fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="1b857-123">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1b857-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="1b857-124">-Name</span></span>
<span data-ttu-id="1b857-125">Especifica o nome do gateway lógico sobre o qual obter informações.</span><span class="sxs-lookup"><span data-stu-id="1b857-125">Specifies the name of the logical gateway about which to get information.</span></span>

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

### <span data-ttu-id="1b857-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b857-126">-ResourceGroupName</span></span>
<span data-ttu-id="1b857-127">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="1b857-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1b857-128">Esse cmdlet obtém informações sobre os gateways lógicos que pertencem ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="1b857-128">This cmdlet gets information about logical gateways that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1b857-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b857-129">-DefaultProfile</span></span>
<span data-ttu-id="1b857-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1b857-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b857-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b857-131">CommonParameters</span></span>
<span data-ttu-id="1b857-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b857-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b857-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b857-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b857-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1b857-134">INPUTS</span></span>

## <span data-ttu-id="1b857-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1b857-135">OUTPUTS</span></span>

### <span data-ttu-id="1b857-136">System. Collections. Generic. List ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway]], Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="1b857-136">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway]], Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway</span></span>

## <span data-ttu-id="1b857-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1b857-137">NOTES</span></span>
* <span data-ttu-id="1b857-138">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="1b857-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1b857-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1b857-139">RELATED LINKS</span></span>

[<span data-ttu-id="1b857-140">New-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="1b857-140">New-AzureRmDataFactoryGateway</span></span>](./New-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="1b857-141">Remove-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="1b857-141">Remove-AzureRmDataFactoryGateway</span></span>](./Remove-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="1b857-142">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="1b857-142">Set-AzureRmDataFactoryGateway</span></span>](./Set-AzureRmDataFactoryGateway.md)


