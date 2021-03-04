---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B07FE1A2-732D-4CCF-A0DF-3CF6B91FB3F3
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
ms.openlocfilehash: 24c9f9631f1a37e218ff8ddf27ad0de54f2d9dbb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888314"
---
# <span data-ttu-id="04e00-101">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="04e00-101">Get-AzDataFactoryHub</span></span>

## <span data-ttu-id="04e00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04e00-102">SYNOPSIS</span></span>
<span data-ttu-id="04e00-103">Obtém informações sobre hubs no Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="04e00-103">Gets information about hubs in Azure Data Factory.</span></span>

## <span data-ttu-id="04e00-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="04e00-104">SYNTAX</span></span>

### <span data-ttu-id="04e00-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="04e00-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04e00-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="04e00-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04e00-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="04e00-107">DESCRIPTION</span></span>
<span data-ttu-id="04e00-108">O cmdlet **Get-AzDataFactoryHub** obtém informações sobre hubs no Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="04e00-108">The **Get-AzDataFactoryHub** cmdlet gets information about hubs in Azure Data Factory.</span></span>
<span data-ttu-id="04e00-109">Se você especificar o nome de um hub, esse cmdlet obterá informações sobre esse hub.</span><span class="sxs-lookup"><span data-stu-id="04e00-109">If you specify the name of a hub, this cmdlet gets information about that hub.</span></span>
<span data-ttu-id="04e00-110">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os hubs em um fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="04e00-110">If you do not specify a name, this cmdlet gets information about all of the hubs in a data factory.</span></span>

## <span data-ttu-id="04e00-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="04e00-111">EXAMPLES</span></span>

### <span data-ttu-id="04e00-112">Exemplo 1: Obter todos os hubs de dados</span><span class="sxs-lookup"><span data-stu-id="04e00-112">Example 1: Get all data hubs</span></span>
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory"
```

<span data-ttu-id="04e00-113">Esse comando obtém todos os hubs de dados no grupo de recursos do Azure chamado ADFResourceGroup e no fábrica de dados chamado ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="04e00-113">This command gets all data hubs in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

### <span data-ttu-id="04e00-114">Exemplo 2: Obter um hub de dados específico</span><span class="sxs-lookup"><span data-stu-id="04e00-114">Example 2: Get a specific data hub</span></span>
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "MyDataHub"
```

<span data-ttu-id="04e00-115">Este comando obtém informações sobre o hub chamado MyDataHub no grupo de recursos do Azure chamado ADFResourceGroup e no fábrica de dados chamado ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="04e00-115">This command gets information about the hub named MyDataHub in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="04e00-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="04e00-116">PARAMETERS</span></span>

### <span data-ttu-id="04e00-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="04e00-117">-DataFactory</span></span>
<span data-ttu-id="04e00-118">Especifica um **objeto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="04e00-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="04e00-119">Este cmdlet obtém informações sobre hubs no fábrica de dados que este parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="04e00-119">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="04e00-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="04e00-120">-DataFactoryName</span></span>
<span data-ttu-id="04e00-121">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="04e00-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="04e00-122">Este cmdlet obtém informações sobre hubs no fábrica de dados que este parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="04e00-122">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="04e00-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04e00-123">-DefaultProfile</span></span>
<span data-ttu-id="04e00-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="04e00-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="04e00-125">-Name</span><span class="sxs-lookup"><span data-stu-id="04e00-125">-Name</span></span>
<span data-ttu-id="04e00-126">Especifica o nome do hub sobre o qual obter informações.</span><span class="sxs-lookup"><span data-stu-id="04e00-126">Specifies the name of the hub about which to get information.</span></span>

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

### <span data-ttu-id="04e00-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04e00-127">-ResourceGroupName</span></span>
<span data-ttu-id="04e00-128">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="04e00-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="04e00-129">Este cmdlet obtém informações sobre hubs que pertencem ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="04e00-129">This cmdlet gets information about hubs that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="04e00-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04e00-130">CommonParameters</span></span>
<span data-ttu-id="04e00-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04e00-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04e00-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04e00-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04e00-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="04e00-133">INPUTS</span></span>

### <span data-ttu-id="04e00-134">System.String</span><span class="sxs-lookup"><span data-stu-id="04e00-134">System.String</span></span>

### <span data-ttu-id="04e00-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="04e00-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="04e00-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="04e00-136">OUTPUTS</span></span>

### <span data-ttu-id="04e00-137">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span><span class="sxs-lookup"><span data-stu-id="04e00-137">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="04e00-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="04e00-138">NOTES</span></span>
* <span data-ttu-id="04e00-139">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="04e00-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="04e00-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="04e00-140">RELATED LINKS</span></span>

[<span data-ttu-id="04e00-141">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="04e00-141">New-AzDataFactoryHub</span></span>](./New-AzDataFactoryHub.md)

[<span data-ttu-id="04e00-142">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="04e00-142">Remove-AzDataFactoryHub</span></span>](./Remove-AzDataFactoryHub.md)


