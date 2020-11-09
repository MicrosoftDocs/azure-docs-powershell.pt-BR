---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B07FE1A2-732D-4CCF-A0DF-3CF6B91FB3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
ms.openlocfilehash: 292a288850371a834f938143cf2ec4380504091b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281080"
---
# <span data-ttu-id="7bfc7-101">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="7bfc7-101">Get-AzDataFactoryHub</span></span>

## <span data-ttu-id="7bfc7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7bfc7-102">SYNOPSIS</span></span>
<span data-ttu-id="7bfc7-103">Obtém informações sobre hubs no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="7bfc7-103">Gets information about hubs in Azure Data Factory.</span></span>

## <span data-ttu-id="7bfc7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7bfc7-104">SYNTAX</span></span>

### <span data-ttu-id="7bfc7-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="7bfc7-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7bfc7-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="7bfc7-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bfc7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7bfc7-107">DESCRIPTION</span></span>
<span data-ttu-id="7bfc7-108">O cmdlet **Get-AzDataFactoryHub** Obtém informações sobre hubs no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="7bfc7-108">The **Get-AzDataFactoryHub** cmdlet gets information about hubs in Azure Data Factory.</span></span>
<span data-ttu-id="7bfc7-109">Se você especificar o nome de um Hub, esse cmdlet obterá informações sobre esse Hub.</span><span class="sxs-lookup"><span data-stu-id="7bfc7-109">If you specify the name of a hub, this cmdlet gets information about that hub.</span></span>
<span data-ttu-id="7bfc7-110">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os hubs em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="7bfc7-110">If you do not specify a name, this cmdlet gets information about all of the hubs in a data factory.</span></span>

## <span data-ttu-id="7bfc7-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7bfc7-111">EXAMPLES</span></span>

### <span data-ttu-id="7bfc7-112">Exemplo 1: obter todos os hubs de dados</span><span class="sxs-lookup"><span data-stu-id="7bfc7-112">Example 1: Get all data hubs</span></span>
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory"
```

<span data-ttu-id="7bfc7-113">Esse comando obtém todos os hubs de dados no grupo de recursos do Azure chamado ADFResourceGroup e o data Factory chamado ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="7bfc7-113">This command gets all data hubs in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

### <span data-ttu-id="7bfc7-114">Exemplo 2: obter um hub de dados específico</span><span class="sxs-lookup"><span data-stu-id="7bfc7-114">Example 2: Get a specific data hub</span></span>
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "MyDataHub"
```

<span data-ttu-id="7bfc7-115">Esse comando obtém informações sobre o Hub chamado MyDataHub no grupo de recursos do Azure chamado ADFResourceGroup e o data Factory chamado ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="7bfc7-115">This command gets information about the hub named MyDataHub in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="7bfc7-116">OS</span><span class="sxs-lookup"><span data-stu-id="7bfc7-116">PARAMETERS</span></span>

### <span data-ttu-id="7bfc7-117">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="7bfc7-117">-DataFactory</span></span>
<span data-ttu-id="7bfc7-118">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="7bfc7-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="7bfc7-119">Esse cmdlet obtém informações sobre hubs na fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="7bfc7-119">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="7bfc7-120">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="7bfc7-120">-DataFactoryName</span></span>
<span data-ttu-id="7bfc7-121">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="7bfc7-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="7bfc7-122">Esse cmdlet obtém informações sobre hubs na fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="7bfc7-122">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="7bfc7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bfc7-123">-DefaultProfile</span></span>
<span data-ttu-id="7bfc7-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7bfc7-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7bfc7-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="7bfc7-125">-Name</span></span>
<span data-ttu-id="7bfc7-126">Especifica o nome do Hub sobre o qual obter informações.</span><span class="sxs-lookup"><span data-stu-id="7bfc7-126">Specifies the name of the hub about which to get information.</span></span>

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

### <span data-ttu-id="7bfc7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bfc7-127">-ResourceGroupName</span></span>
<span data-ttu-id="7bfc7-128">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="7bfc7-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="7bfc7-129">Esse cmdlet obtém informações sobre hubs que pertencem ao grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="7bfc7-129">This cmdlet gets information about hubs that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7bfc7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bfc7-130">CommonParameters</span></span>
<span data-ttu-id="7bfc7-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bfc7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bfc7-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bfc7-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bfc7-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7bfc7-133">INPUTS</span></span>

### <span data-ttu-id="7bfc7-134">System. String</span><span class="sxs-lookup"><span data-stu-id="7bfc7-134">System.String</span></span>

### <span data-ttu-id="7bfc7-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="7bfc7-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="7bfc7-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7bfc7-136">OUTPUTS</span></span>

### <span data-ttu-id="7bfc7-137">Microsoft. Azure. Commands. datafactorings. Models. PSHub</span><span class="sxs-lookup"><span data-stu-id="7bfc7-137">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="7bfc7-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7bfc7-138">NOTES</span></span>
* <span data-ttu-id="7bfc7-139">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="7bfc7-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="7bfc7-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7bfc7-140">RELATED LINKS</span></span>

[<span data-ttu-id="7bfc7-141">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="7bfc7-141">New-AzDataFactoryHub</span></span>](./New-AzDataFactoryHub.md)

[<span data-ttu-id="7bfc7-142">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="7bfc7-142">Remove-AzDataFactoryHub</span></span>](./Remove-AzDataFactoryHub.md)


