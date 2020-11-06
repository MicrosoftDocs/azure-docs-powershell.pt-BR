---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 9425D38D-5978-421F-A438-4463068C4628
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryLinkedService.md
ms.openlocfilehash: 94321cc8f9d42cd4ef26e617426f844b9774b5b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430505"
---
# <span data-ttu-id="c21ce-101">Remove-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="c21ce-101">Remove-AzureRmDataFactoryLinkedService</span></span>

## <span data-ttu-id="c21ce-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c21ce-102">SYNOPSIS</span></span>
<span data-ttu-id="c21ce-103">Remove um serviço vinculado do Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="c21ce-103">Removes a linked service from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c21ce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c21ce-104">SYNTAX</span></span>

### <span data-ttu-id="c21ce-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="c21ce-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryLinkedService [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c21ce-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c21ce-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryLinkedService [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c21ce-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c21ce-107">DESCRIPTION</span></span>
<span data-ttu-id="c21ce-108">O cmdlet **Remove-AzureRmDataFactoryLinkedService** remove um serviço vinculado do Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="c21ce-108">The **Remove-AzureRmDataFactoryLinkedService** cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="c21ce-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c21ce-109">EXAMPLES</span></span>

### <span data-ttu-id="c21ce-110">Exemplo 1: remover um serviço vinculado</span><span class="sxs-lookup"><span data-stu-id="c21ce-110">Example 1: Remove a linked service</span></span>
```
PS C:\>Remove-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
Confirm
Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="c21ce-111">Esse comando Remove o serviço vinculado denominado LinkedServiceTest do data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="c21ce-111">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="c21ce-112">Esse comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="c21ce-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="c21ce-113">OS</span><span class="sxs-lookup"><span data-stu-id="c21ce-113">PARAMETERS</span></span>

### <span data-ttu-id="c21ce-114">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="c21ce-114">-DataFactory</span></span>
<span data-ttu-id="c21ce-115">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="c21ce-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="c21ce-116">Esse cmdlet Remove um serviço vinculado do alocador de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="c21ce-116">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c21ce-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="c21ce-117">-DataFactoryName</span></span>
<span data-ttu-id="c21ce-118">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="c21ce-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="c21ce-119">Esse cmdlet Remove um serviço vinculado do alocador de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="c21ce-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c21ce-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c21ce-120">-DefaultProfile</span></span>
<span data-ttu-id="c21ce-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c21ce-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c21ce-122">-Force</span><span class="sxs-lookup"><span data-stu-id="c21ce-122">-Force</span></span>
<span data-ttu-id="c21ce-123">Indica que esse cmdlet Remove um serviço vinculado sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="c21ce-123">Indicates that this cmdlet removes a linked service without prompting you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c21ce-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="c21ce-124">-Name</span></span>
<span data-ttu-id="c21ce-125">Especifica o nome do serviço vinculado a ser removido.</span><span class="sxs-lookup"><span data-stu-id="c21ce-125">Specifies the name of the linked service to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c21ce-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c21ce-126">-ResourceGroupName</span></span>
<span data-ttu-id="c21ce-127">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="c21ce-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c21ce-128">Esse cmdlet Remove um serviço vinculado do grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="c21ce-128">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c21ce-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c21ce-129">-Confirm</span></span>
<span data-ttu-id="c21ce-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c21ce-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c21ce-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c21ce-131">-WhatIf</span></span>
<span data-ttu-id="c21ce-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c21ce-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c21ce-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c21ce-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c21ce-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c21ce-134">CommonParameters</span></span>
<span data-ttu-id="c21ce-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c21ce-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c21ce-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c21ce-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c21ce-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c21ce-137">INPUTS</span></span>

### <span data-ttu-id="c21ce-138">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c21ce-138">None</span></span>
<span data-ttu-id="c21ce-139">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="c21ce-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c21ce-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c21ce-140">OUTPUTS</span></span>

### <span data-ttu-id="c21ce-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c21ce-141">System.Boolean</span></span>

## <span data-ttu-id="c21ce-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c21ce-142">NOTES</span></span>
* <span data-ttu-id="c21ce-143">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="c21ce-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c21ce-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c21ce-144">RELATED LINKS</span></span>

[<span data-ttu-id="c21ce-145">Get-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="c21ce-145">Get-AzureRmDataFactoryLinkedService</span></span>](./Get-AzureRmDataFactoryLinkedService.md)

[<span data-ttu-id="c21ce-146">New-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="c21ce-146">New-AzureRmDataFactoryLinkedService</span></span>](./New-AzureRmDataFactoryLinkedService.md)


