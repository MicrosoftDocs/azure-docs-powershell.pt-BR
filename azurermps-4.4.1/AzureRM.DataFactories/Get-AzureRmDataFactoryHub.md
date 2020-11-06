---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: B07FE1A2-732D-4CCF-A0DF-3CF6B91FB3F3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryHub.md
ms.openlocfilehash: a96d8d3d9025e473b5c08d84201fde2a10d8be34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441143"
---
# <span data-ttu-id="640ba-101">Get-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="640ba-101">Get-AzureRmDataFactoryHub</span></span>

## <span data-ttu-id="640ba-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="640ba-102">SYNOPSIS</span></span>
<span data-ttu-id="640ba-103">Obtém informações sobre hubs no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="640ba-103">Gets information about hubs in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="640ba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="640ba-104">SYNTAX</span></span>

### <span data-ttu-id="640ba-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="640ba-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryHub [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="640ba-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="640ba-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryHub [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="640ba-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="640ba-107">DESCRIPTION</span></span>
<span data-ttu-id="640ba-108">O cmdlet **Get-AzureRmDataFactoryHub** Obtém informações sobre hubs no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="640ba-108">The **Get-AzureRmDataFactoryHub** cmdlet gets information about hubs in Azure Data Factory.</span></span>
<span data-ttu-id="640ba-109">Se você especificar o nome de um Hub, esse cmdlet obterá informações sobre esse Hub.</span><span class="sxs-lookup"><span data-stu-id="640ba-109">If you specify the name of a hub, this cmdlet gets information about that hub.</span></span>
<span data-ttu-id="640ba-110">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os hubs em uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="640ba-110">If you do not specify a name, this cmdlet gets information about all of the hubs in a data factory.</span></span>

## <span data-ttu-id="640ba-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="640ba-111">EXAMPLES</span></span>

### <span data-ttu-id="640ba-112">Exemplo 1: obter todos os hubs de dados</span><span class="sxs-lookup"><span data-stu-id="640ba-112">Example 1: Get all data hubs</span></span>
```
PS C:\>Get-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory"
```

<span data-ttu-id="640ba-113">Esse comando obtém todos os hubs de dados no grupo de recursos do Azure chamado ADFResourceGroup e o data Factory chamado ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="640ba-113">This command gets all data hubs in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

### <span data-ttu-id="640ba-114">Exemplo 2: obter um hub de dados específico</span><span class="sxs-lookup"><span data-stu-id="640ba-114">Example 2: Get a specific data hub</span></span>
```
PS C:\>Get-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "MyDataHub"
```

<span data-ttu-id="640ba-115">Esse comando obtém informações sobre o Hub chamado MyDataHub no grupo de recursos do Azure chamado ADFResourceGroup e o data Factory chamado ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="640ba-115">This command gets information about the hub named MyDataHub in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="640ba-116">OS</span><span class="sxs-lookup"><span data-stu-id="640ba-116">PARAMETERS</span></span>

### <span data-ttu-id="640ba-117">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="640ba-117">-DataFactory</span></span>
<span data-ttu-id="640ba-118">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="640ba-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="640ba-119">Esse cmdlet obtém informações sobre hubs na fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="640ba-119">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="640ba-120">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="640ba-120">-DataFactoryName</span></span>
<span data-ttu-id="640ba-121">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="640ba-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="640ba-122">Esse cmdlet obtém informações sobre hubs na fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="640ba-122">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="640ba-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="640ba-123">-Name</span></span>
<span data-ttu-id="640ba-124">Especifica o nome do Hub sobre o qual obter informações.</span><span class="sxs-lookup"><span data-stu-id="640ba-124">Specifies the name of the hub about which to get information.</span></span>

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

### <span data-ttu-id="640ba-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="640ba-125">-ResourceGroupName</span></span>
<span data-ttu-id="640ba-126">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="640ba-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="640ba-127">Esse cmdlet obtém informações sobre hubs que pertencem ao grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="640ba-127">This cmdlet gets information about hubs that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="640ba-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="640ba-128">-DefaultProfile</span></span>
<span data-ttu-id="640ba-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="640ba-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="640ba-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="640ba-130">CommonParameters</span></span>
<span data-ttu-id="640ba-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="640ba-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="640ba-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="640ba-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="640ba-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="640ba-133">INPUTS</span></span>

## <span data-ttu-id="640ba-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="640ba-134">OUTPUTS</span></span>

### <span data-ttu-id="640ba-135">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. datafactorings. Models. PSHub]</span><span class="sxs-lookup"><span data-stu-id="640ba-135">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.DataFactories.Models.PSHub]</span></span>

### <span data-ttu-id="640ba-136">Microsoft. Azure. Commands. datafactorings. Models. PSHub</span><span class="sxs-lookup"><span data-stu-id="640ba-136">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="640ba-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="640ba-137">NOTES</span></span>
* <span data-ttu-id="640ba-138">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="640ba-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="640ba-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="640ba-139">RELATED LINKS</span></span>

[<span data-ttu-id="640ba-140">New-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="640ba-140">New-AzureRmDataFactoryHub</span></span>](./New-AzureRmDataFactoryHub.md)

[<span data-ttu-id="640ba-141">Remove-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="640ba-141">Remove-AzureRmDataFactoryHub</span></span>](./Remove-AzureRmDataFactoryHub.md)

