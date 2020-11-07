---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 4C839730-B494-45BD-B5A1-F93B02AB4B2A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryHub.md
ms.openlocfilehash: 12a18c62d3cc3412726df323bd48acd86ed7b1fd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778320"
---
# <span data-ttu-id="4301d-101">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="4301d-101">Remove-AzDataFactoryHub</span></span>

## <span data-ttu-id="4301d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4301d-102">SYNOPSIS</span></span>
<span data-ttu-id="4301d-103">Remove um Hub do Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="4301d-103">Removes a hub from Azure Data Factory.</span></span>

## <span data-ttu-id="4301d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4301d-104">SYNTAX</span></span>

### <span data-ttu-id="4301d-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="4301d-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryHub [-Name] <String> [-Force] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4301d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4301d-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryHub [-Name] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4301d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4301d-107">DESCRIPTION</span></span>
<span data-ttu-id="4301d-108">O cmdlet **Remove-AzDataFactoryHub** remove um Hub do Azure data Factory no grupo de recursos do Azure especificado e na fábrica de dados especificada.</span><span class="sxs-lookup"><span data-stu-id="4301d-108">The **Remove-AzDataFactoryHub** cmdlet removes a hub from Azure Data Factory in the specified Azure resource group and in the specified data factory.</span></span>
<span data-ttu-id="4301d-109">Se você remover um Hub, todos os serviços vinculados e pipelines no Hub também serão removidos.</span><span class="sxs-lookup"><span data-stu-id="4301d-109">If you remove a hub, all linked services and pipelines in the hub are also removed.</span></span>

## <span data-ttu-id="4301d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4301d-110">EXAMPLES</span></span>

### <span data-ttu-id="4301d-111">Exemplo 1: remover um hub</span><span class="sxs-lookup"><span data-stu-id="4301d-111">Example 1: Remove a hub</span></span>
```
PS C:\>Remove-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub"
```

<span data-ttu-id="4301d-112">Esse comando Remove o Hub chamado ContosoDataHub do grupo de recursos do Azure chamado ADFResourceGroup e o data Factory chamado ADFDataFactory.</span><span class="sxs-lookup"><span data-stu-id="4301d-112">This command removes the hub named ContosoDataHub from the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="4301d-113">OS</span><span class="sxs-lookup"><span data-stu-id="4301d-113">PARAMETERS</span></span>

### <span data-ttu-id="4301d-114">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="4301d-114">-DataFactory</span></span>
<span data-ttu-id="4301d-115">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="4301d-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="4301d-116">Esse cmdlet Remove um Hub da fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="4301d-116">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4301d-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="4301d-117">-DataFactoryName</span></span>
<span data-ttu-id="4301d-118">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="4301d-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="4301d-119">Esse cmdlet Remove um Hub da fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="4301d-119">This cmdlet removes a hub from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4301d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4301d-120">-DefaultProfile</span></span>
<span data-ttu-id="4301d-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4301d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4301d-122">-Force</span><span class="sxs-lookup"><span data-stu-id="4301d-122">-Force</span></span>
<span data-ttu-id="4301d-123">Indica que esse cmdlet Remove um Hub sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="4301d-123">Indicates that this cmdlet removes a hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="4301d-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="4301d-124">-Name</span></span>
<span data-ttu-id="4301d-125">Especifica o nome do hub a ser removido.</span><span class="sxs-lookup"><span data-stu-id="4301d-125">Specifies the name of the hub to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4301d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4301d-126">-ResourceGroupName</span></span>
<span data-ttu-id="4301d-127">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="4301d-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="4301d-128">Esse cmdlet Remove um Hub do grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="4301d-128">This cmdlet removes a hub from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4301d-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4301d-129">-Confirm</span></span>
<span data-ttu-id="4301d-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4301d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4301d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4301d-131">-WhatIf</span></span>
<span data-ttu-id="4301d-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4301d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4301d-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4301d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4301d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4301d-134">CommonParameters</span></span>
<span data-ttu-id="4301d-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4301d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4301d-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4301d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4301d-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4301d-137">INPUTS</span></span>

### <span data-ttu-id="4301d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4301d-138">System.String</span></span>

### <span data-ttu-id="4301d-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="4301d-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="4301d-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4301d-140">OUTPUTS</span></span>

### <span data-ttu-id="4301d-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4301d-141">System.Boolean</span></span>

## <span data-ttu-id="4301d-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4301d-142">NOTES</span></span>
* <span data-ttu-id="4301d-143">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="4301d-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="4301d-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4301d-144">RELATED LINKS</span></span>

[<span data-ttu-id="4301d-145">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="4301d-145">Get-AzDataFactoryHub</span></span>](./Get-AzDataFactoryHub.md)

[<span data-ttu-id="4301d-146">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="4301d-146">New-AzDataFactoryHub</span></span>](./New-AzDataFactoryHub.md)


