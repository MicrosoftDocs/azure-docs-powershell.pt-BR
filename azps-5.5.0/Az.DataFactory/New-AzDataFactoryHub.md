---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B656B4C4-97DE-4F9F-937C-E115CB3F0E80
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryHub.md
ms.openlocfilehash: 1155b7c0b294ac3bc5c2106b473ce1cf55a9ac82
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113282"
---
# <span data-ttu-id="42bc7-101">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="42bc7-101">New-AzDataFactoryHub</span></span>

## <span data-ttu-id="42bc7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="42bc7-102">SYNOPSIS</span></span>
<span data-ttu-id="42bc7-103">Cria um hub para uma Fábrica de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="42bc7-103">Creates a hub for an Azure Data Factory.</span></span>

## <span data-ttu-id="42bc7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="42bc7-104">SYNTAX</span></span>

### <span data-ttu-id="42bc7-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="42bc7-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="42bc7-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="42bc7-106">ByFactoryObject</span></span>
```
New-AzDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42bc7-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="42bc7-107">DESCRIPTION</span></span>
<span data-ttu-id="42bc7-108">O cmdlet **New-AzDataFactoryHub** cria um hub para o Azure Data Factory no grupo de recursos do Azure especificado e no fábrica de dados especificado com a definição de arquivo especificada.</span><span class="sxs-lookup"><span data-stu-id="42bc7-108">The **New-AzDataFactoryHub** cmdlet creates a hub for Azure Data Factory in the specified Azure resource group and in the specified data factory with the specified file definition.</span></span>
<span data-ttu-id="42bc7-109">Depois de criar o hub, você pode usá-lo para armazenar e gerenciar serviços vinculados em um grupo e adicionar pipelines ao hub.</span><span class="sxs-lookup"><span data-stu-id="42bc7-109">After you create the hub, you can use it to store and manage linked services in a group, and you can add pipelines to the hub.</span></span>

## <span data-ttu-id="42bc7-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="42bc7-110">EXAMPLES</span></span>

### <span data-ttu-id="42bc7-111">Exemplo 1: Criar um hub</span><span class="sxs-lookup"><span data-stu-id="42bc7-111">Example 1: Create a hub</span></span>
```
PS C:\>New-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub" -File "C:\Hub.json"
```

<span data-ttu-id="42bc7-112">Esse comando cria um hub chamado ContosoDataHub no grupo de recursos ADFResourceGroup e no fábrica de dados chamado ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="42bc7-112">This command creates a hub named ContosoDataHub in the resource group ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="42bc7-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="42bc7-113">PARAMETERS</span></span>

### <span data-ttu-id="42bc7-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="42bc7-114">-DataFactory</span></span>
<span data-ttu-id="42bc7-115">Especifica um **objeto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="42bc7-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="42bc7-116">Este cmdlet cria um hub para a fábrica de dados especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="42bc7-116">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="42bc7-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="42bc7-117">-DataFactoryName</span></span>
<span data-ttu-id="42bc7-118">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="42bc7-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="42bc7-119">Este cmdlet cria um hub para a fábrica de dados especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="42bc7-119">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="42bc7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42bc7-120">-DefaultProfile</span></span>
<span data-ttu-id="42bc7-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="42bc7-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42bc7-122">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="42bc7-122">-File</span></span>
<span data-ttu-id="42bc7-123">Especifica o caminho completo do arquivo JSON (Notação de Objeto JavaScript) que contém a descrição do hub.</span><span class="sxs-lookup"><span data-stu-id="42bc7-123">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the hub.</span></span>

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

### <span data-ttu-id="42bc7-124">-Forçar</span><span class="sxs-lookup"><span data-stu-id="42bc7-124">-Force</span></span>
<span data-ttu-id="42bc7-125">Indica que esse cmdlet substitui um hub existente sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="42bc7-125">Indicates that this cmdlet replaces an existing hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="42bc7-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="42bc7-126">-Name</span></span>
<span data-ttu-id="42bc7-127">Especifica o nome do hub a ser criado.</span><span class="sxs-lookup"><span data-stu-id="42bc7-127">Specifies the name of the hub to create.</span></span>

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

### <span data-ttu-id="42bc7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42bc7-128">-ResourceGroupName</span></span>
<span data-ttu-id="42bc7-129">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="42bc7-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="42bc7-130">Esse cmdlet cria um hub que pertence ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="42bc7-130">This cmdlet creates a hub that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="42bc7-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="42bc7-131">-Confirm</span></span>
<span data-ttu-id="42bc7-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42bc7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42bc7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42bc7-133">-WhatIf</span></span>
<span data-ttu-id="42bc7-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="42bc7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42bc7-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="42bc7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42bc7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42bc7-136">CommonParameters</span></span>
<span data-ttu-id="42bc7-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42bc7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42bc7-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42bc7-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42bc7-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="42bc7-139">INPUTS</span></span>

### <span data-ttu-id="42bc7-140">System.String</span><span class="sxs-lookup"><span data-stu-id="42bc7-140">System.String</span></span>

### <span data-ttu-id="42bc7-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="42bc7-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="42bc7-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="42bc7-142">OUTPUTS</span></span>

### <span data-ttu-id="42bc7-143">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span><span class="sxs-lookup"><span data-stu-id="42bc7-143">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="42bc7-144">Notas</span><span class="sxs-lookup"><span data-stu-id="42bc7-144">NOTES</span></span>
* <span data-ttu-id="42bc7-145">Palavras-chave: azure, azurerm, arm, resource, management, manager, data,</span><span class="sxs-lookup"><span data-stu-id="42bc7-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="42bc7-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="42bc7-146">RELATED LINKS</span></span>

[<span data-ttu-id="42bc7-147">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="42bc7-147">Get-AzDataFactoryHub</span></span>](./Get-AzDataFactoryHub.md)

[<span data-ttu-id="42bc7-148">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="42bc7-148">Remove-AzDataFactoryHub</span></span>](./Remove-AzDataFactoryHub.md)


