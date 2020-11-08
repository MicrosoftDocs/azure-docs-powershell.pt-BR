---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B656B4C4-97DE-4F9F-937C-E115CB3F0E80
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryHub.md
ms.openlocfilehash: 1155b7c0b294ac3bc5c2106b473ce1cf55a9ac82
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112320"
---
# <span data-ttu-id="c3016-101">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="c3016-101">New-AzDataFactoryHub</span></span>

## <span data-ttu-id="c3016-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c3016-102">SYNOPSIS</span></span>
<span data-ttu-id="c3016-103">Cria um hub para uma fábrica de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="c3016-103">Creates a hub for an Azure Data Factory.</span></span>

## <span data-ttu-id="c3016-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3016-104">SYNTAX</span></span>

### <span data-ttu-id="c3016-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="c3016-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c3016-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c3016-106">ByFactoryObject</span></span>
```
New-AzDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3016-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c3016-107">DESCRIPTION</span></span>
<span data-ttu-id="c3016-108">O cmdlet **New-AzDataFactoryHub** cria um Hub do Azure data Factory no grupo de recursos do Azure especificado e na fábrica de dados especificada com a definição de arquivo especificada.</span><span class="sxs-lookup"><span data-stu-id="c3016-108">The **New-AzDataFactoryHub** cmdlet creates a hub for Azure Data Factory in the specified Azure resource group and in the specified data factory with the specified file definition.</span></span>
<span data-ttu-id="c3016-109">Depois de criar o Hub, você pode usá-lo para armazenar e gerenciar serviços vinculados em um grupo, e pode adicionar pipelines ao Hub.</span><span class="sxs-lookup"><span data-stu-id="c3016-109">After you create the hub, you can use it to store and manage linked services in a group, and you can add pipelines to the hub.</span></span>

## <span data-ttu-id="c3016-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c3016-110">EXAMPLES</span></span>

### <span data-ttu-id="c3016-111">Exemplo 1: criar um hub</span><span class="sxs-lookup"><span data-stu-id="c3016-111">Example 1: Create a hub</span></span>
```
PS C:\>New-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub" -File "C:\Hub.json"
```

<span data-ttu-id="c3016-112">Esse comando cria um Hub chamado ContosoDataHub na ADFResourceGroup do grupo de recursos e na fábrica de dados chamada ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="c3016-112">This command creates a hub named ContosoDataHub in the resource group ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="c3016-113">OS</span><span class="sxs-lookup"><span data-stu-id="c3016-113">PARAMETERS</span></span>

### <span data-ttu-id="c3016-114">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="c3016-114">-DataFactory</span></span>
<span data-ttu-id="c3016-115">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="c3016-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="c3016-116">Esse cmdlet cria um hub para a fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="c3016-116">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="c3016-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="c3016-117">-DataFactoryName</span></span>
<span data-ttu-id="c3016-118">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="c3016-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="c3016-119">Esse cmdlet cria um hub para a fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="c3016-119">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="c3016-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3016-120">-DefaultProfile</span></span>
<span data-ttu-id="c3016-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c3016-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3016-122">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="c3016-122">-File</span></span>
<span data-ttu-id="c3016-123">Especifica o caminho completo do arquivo JSON (JavaScript Object Notation) que contém a descrição do Hub.</span><span class="sxs-lookup"><span data-stu-id="c3016-123">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the hub.</span></span>

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

### <span data-ttu-id="c3016-124">-Force</span><span class="sxs-lookup"><span data-stu-id="c3016-124">-Force</span></span>
<span data-ttu-id="c3016-125">Indica que esse cmdlet substitui um Hub existente sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="c3016-125">Indicates that this cmdlet replaces an existing hub without prompting you for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3016-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="c3016-126">-Name</span></span>
<span data-ttu-id="c3016-127">Especifica o nome do hub a ser criado.</span><span class="sxs-lookup"><span data-stu-id="c3016-127">Specifies the name of the hub to create.</span></span>

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

### <span data-ttu-id="c3016-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3016-128">-ResourceGroupName</span></span>
<span data-ttu-id="c3016-129">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="c3016-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c3016-130">Esse cmdlet cria um Hub que pertence ao grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="c3016-130">This cmdlet creates a hub that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c3016-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c3016-131">-Confirm</span></span>
<span data-ttu-id="c3016-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3016-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3016-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3016-133">-WhatIf</span></span>
<span data-ttu-id="c3016-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c3016-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3016-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c3016-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3016-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3016-136">CommonParameters</span></span>
<span data-ttu-id="c3016-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3016-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3016-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3016-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3016-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c3016-139">INPUTS</span></span>

### <span data-ttu-id="c3016-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c3016-140">System.String</span></span>

### <span data-ttu-id="c3016-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="c3016-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="c3016-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c3016-142">OUTPUTS</span></span>

### <span data-ttu-id="c3016-143">Microsoft. Azure. Commands. datafactorings. Models. PSHub</span><span class="sxs-lookup"><span data-stu-id="c3016-143">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="c3016-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c3016-144">NOTES</span></span>
* <span data-ttu-id="c3016-145">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="c3016-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c3016-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c3016-146">RELATED LINKS</span></span>

[<span data-ttu-id="c3016-147">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="c3016-147">Get-AzDataFactoryHub</span></span>](./Get-AzDataFactoryHub.md)

[<span data-ttu-id="c3016-148">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="c3016-148">Remove-AzDataFactoryHub</span></span>](./Remove-AzDataFactoryHub.md)


