---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: B656B4C4-97DE-4F9F-937C-E115CB3F0E80
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryHub.md
ms.openlocfilehash: d92cb12f051095a7e5de47d9c12b2c2329841bd3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430745"
---
# <span data-ttu-id="4351b-101">New-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="4351b-101">New-AzureRmDataFactoryHub</span></span>

## <span data-ttu-id="4351b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4351b-102">SYNOPSIS</span></span>
<span data-ttu-id="4351b-103">Cria um hub para uma fábrica de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="4351b-103">Creates a hub for an Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4351b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4351b-104">SYNTAX</span></span>

### <span data-ttu-id="4351b-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="4351b-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4351b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4351b-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4351b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4351b-107">DESCRIPTION</span></span>
<span data-ttu-id="4351b-108">O cmdlet **New-AzureRmDataFactoryHub** cria um Hub do Azure data Factory no grupo de recursos do Azure especificado e na fábrica de dados especificada com a definição de arquivo especificada.</span><span class="sxs-lookup"><span data-stu-id="4351b-108">The **New-AzureRmDataFactoryHub** cmdlet creates a hub for Azure Data Factory in the specified Azure resource group and in the specified data factory with the specified file definition.</span></span>
<span data-ttu-id="4351b-109">Depois de criar o Hub, você pode usá-lo para armazenar e gerenciar serviços vinculados em um grupo, e pode adicionar pipelines ao Hub.</span><span class="sxs-lookup"><span data-stu-id="4351b-109">After you create the hub, you can use it to store and manage linked services in a group, and you can add pipelines to the hub.</span></span>

## <span data-ttu-id="4351b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4351b-110">EXAMPLES</span></span>

### <span data-ttu-id="4351b-111">Exemplo 1: criar um hub</span><span class="sxs-lookup"><span data-stu-id="4351b-111">Example 1: Create a hub</span></span>
```
PS C:\>New-AzureRmDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub" -File "C:\Hub.json"
```

<span data-ttu-id="4351b-112">Esse comando cria um Hub chamado ContosoDataHub na ADFResourceGroup do grupo de recursos e na fábrica de dados chamada ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="4351b-112">This command creates a hub named ContosoDataHub in the resource group ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="4351b-113">OS</span><span class="sxs-lookup"><span data-stu-id="4351b-113">PARAMETERS</span></span>

### <span data-ttu-id="4351b-114">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="4351b-114">-DataFactory</span></span>
<span data-ttu-id="4351b-115">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="4351b-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="4351b-116">Esse cmdlet cria um hub para a fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="4351b-116">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4351b-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="4351b-117">-DataFactoryName</span></span>
<span data-ttu-id="4351b-118">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="4351b-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="4351b-119">Esse cmdlet cria um hub para a fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="4351b-119">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4351b-120">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="4351b-120">-File</span></span>
<span data-ttu-id="4351b-121">Especifica o caminho completo do arquivo JSON (JavaScript Object Notation) que contém a descrição do Hub.</span><span class="sxs-lookup"><span data-stu-id="4351b-121">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the hub.</span></span>

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

### <span data-ttu-id="4351b-122">-Force</span><span class="sxs-lookup"><span data-stu-id="4351b-122">-Force</span></span>
<span data-ttu-id="4351b-123">Indica que esse cmdlet substitui um Hub existente sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="4351b-123">Indicates that this cmdlet replaces an existing hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="4351b-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="4351b-124">-Name</span></span>
<span data-ttu-id="4351b-125">Especifica o nome do hub a ser criado.</span><span class="sxs-lookup"><span data-stu-id="4351b-125">Specifies the name of the hub to create.</span></span>

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

### <span data-ttu-id="4351b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4351b-126">-ResourceGroupName</span></span>
<span data-ttu-id="4351b-127">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="4351b-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="4351b-128">Esse cmdlet cria um Hub que pertence ao grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="4351b-128">This cmdlet creates a hub that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4351b-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4351b-129">-Confirm</span></span>
<span data-ttu-id="4351b-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4351b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4351b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4351b-131">-WhatIf</span></span>
<span data-ttu-id="4351b-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4351b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4351b-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4351b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4351b-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4351b-134">-DefaultProfile</span></span>
<span data-ttu-id="4351b-135">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4351b-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4351b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4351b-136">CommonParameters</span></span>
<span data-ttu-id="4351b-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4351b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4351b-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4351b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4351b-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4351b-139">INPUTS</span></span>

## <span data-ttu-id="4351b-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4351b-140">OUTPUTS</span></span>

### <span data-ttu-id="4351b-141">Microsoft. Azure. Commands. datafactorings. Models. PSHub</span><span class="sxs-lookup"><span data-stu-id="4351b-141">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="4351b-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4351b-142">NOTES</span></span>
* <span data-ttu-id="4351b-143">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="4351b-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="4351b-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4351b-144">RELATED LINKS</span></span>

[<span data-ttu-id="4351b-145">Get-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="4351b-145">Get-AzureRmDataFactoryHub</span></span>](./Get-AzureRmDataFactoryHub.md)

[<span data-ttu-id="4351b-146">Remove-AzureRmDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="4351b-146">Remove-AzureRmDataFactoryHub</span></span>](./Remove-AzureRmDataFactoryHub.md)

