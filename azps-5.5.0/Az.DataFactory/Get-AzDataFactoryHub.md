---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B07FE1A2-732D-4CCF-A0DF-3CF6B91FB3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
ms.openlocfilehash: 292a288850371a834f938143cf2ec4380504091b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116439"
---
# <span data-ttu-id="d5824-101">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="d5824-101">Get-AzDataFactoryHub</span></span>

## <span data-ttu-id="d5824-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d5824-102">SYNOPSIS</span></span>
<span data-ttu-id="d5824-103">Obtém informações sobre hubs no Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="d5824-103">Gets information about hubs in Azure Data Factory.</span></span>

## <span data-ttu-id="d5824-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d5824-104">SYNTAX</span></span>

### <span data-ttu-id="d5824-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="d5824-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5824-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d5824-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5824-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d5824-107">DESCRIPTION</span></span>
<span data-ttu-id="d5824-108">O cmdlet **Get-AzDataFactoryHub** obtém informações sobre hubs no Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="d5824-108">The **Get-AzDataFactoryHub** cmdlet gets information about hubs in Azure Data Factory.</span></span>
<span data-ttu-id="d5824-109">Se você especificar o nome de um hub, esse cmdlet obterá informações sobre esse hub.</span><span class="sxs-lookup"><span data-stu-id="d5824-109">If you specify the name of a hub, this cmdlet gets information about that hub.</span></span>
<span data-ttu-id="d5824-110">Se você não especificar um nome, este cmdlet obterá informações sobre todos os hubs em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="d5824-110">If you do not specify a name, this cmdlet gets information about all of the hubs in a data factory.</span></span>

## <span data-ttu-id="d5824-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d5824-111">EXAMPLES</span></span>

### <span data-ttu-id="d5824-112">Exemplo 1: Obter todos os hubs de dados</span><span class="sxs-lookup"><span data-stu-id="d5824-112">Example 1: Get all data hubs</span></span>
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory"
```

<span data-ttu-id="d5824-113">Esse comando obtém todos os hubs de dados no grupo de recursos do Azure chamado ADFResourceGroup e no fábrica de dados chamado ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="d5824-113">This command gets all data hubs in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

### <span data-ttu-id="d5824-114">Exemplo 2: Obter um hub de dados específico</span><span class="sxs-lookup"><span data-stu-id="d5824-114">Example 2: Get a specific data hub</span></span>
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "MyDataHub"
```

<span data-ttu-id="d5824-115">Esse comando obtém informações sobre o hub chamado MyDataHub no grupo de recursos do Azure chamado ADFResourceGroup e a fábrica de dados chamada ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="d5824-115">This command gets information about the hub named MyDataHub in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="d5824-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5824-116">PARAMETERS</span></span>

### <span data-ttu-id="d5824-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d5824-117">-DataFactory</span></span>
<span data-ttu-id="d5824-118">Especifica um **objeto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="d5824-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="d5824-119">Este cmdlet obtém informações sobre hubs no fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d5824-119">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d5824-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d5824-120">-DataFactoryName</span></span>
<span data-ttu-id="d5824-121">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="d5824-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d5824-122">Este cmdlet obtém informações sobre hubs no fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d5824-122">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d5824-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5824-123">-DefaultProfile</span></span>
<span data-ttu-id="d5824-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="d5824-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5824-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="d5824-125">-Name</span></span>
<span data-ttu-id="d5824-126">Especifica o nome do hub sobre o qual obter informações.</span><span class="sxs-lookup"><span data-stu-id="d5824-126">Specifies the name of the hub about which to get information.</span></span>

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

### <span data-ttu-id="d5824-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5824-127">-ResourceGroupName</span></span>
<span data-ttu-id="d5824-128">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="d5824-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d5824-129">Este cmdlet obtém informações sobre hubs que pertencem ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d5824-129">This cmdlet gets information about hubs that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d5824-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5824-130">CommonParameters</span></span>
<span data-ttu-id="d5824-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5824-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5824-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5824-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5824-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="d5824-133">INPUTS</span></span>

### <span data-ttu-id="d5824-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d5824-134">System.String</span></span>

### <span data-ttu-id="d5824-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d5824-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="d5824-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="d5824-136">OUTPUTS</span></span>

### <span data-ttu-id="d5824-137">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span><span class="sxs-lookup"><span data-stu-id="d5824-137">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="d5824-138">Notas</span><span class="sxs-lookup"><span data-stu-id="d5824-138">NOTES</span></span>
* <span data-ttu-id="d5824-139">Palavras-chave: azure, azurerm, arm, resource, management, manager, data,</span><span class="sxs-lookup"><span data-stu-id="d5824-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d5824-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d5824-140">RELATED LINKS</span></span>

[<span data-ttu-id="d5824-141">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="d5824-141">New-AzDataFactoryHub</span></span>](./New-AzDataFactoryHub.md)

[<span data-ttu-id="d5824-142">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="d5824-142">Remove-AzDataFactoryHub</span></span>](./Remove-AzDataFactoryHub.md)


