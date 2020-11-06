---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 9425D38D-5978-421F-A438-4463068C4628
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryLinkedService.md
ms.openlocfilehash: 7b4dd01a689e1ac7b87e1c83a1e19bbd0c8a86db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602980"
---
# <span data-ttu-id="9637f-101">Remove-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="9637f-101">Remove-AzureRmDataFactoryLinkedService</span></span>

## <span data-ttu-id="9637f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9637f-102">SYNOPSIS</span></span>
<span data-ttu-id="9637f-103">Remove um serviço vinculado do Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="9637f-103">Removes a linked service from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9637f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9637f-104">SYNTAX</span></span>

### <span data-ttu-id="9637f-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="9637f-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryLinkedService [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9637f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9637f-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryLinkedService [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9637f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9637f-107">DESCRIPTION</span></span>
<span data-ttu-id="9637f-108">O cmdlet **Remove-AzureRmDataFactoryLinkedService** remove um serviço vinculado do Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="9637f-108">The **Remove-AzureRmDataFactoryLinkedService** cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="9637f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9637f-109">EXAMPLES</span></span>

### <span data-ttu-id="9637f-110">Exemplo 1: remover um serviço vinculado</span><span class="sxs-lookup"><span data-stu-id="9637f-110">Example 1: Remove a linked service</span></span>
```
PS C:\>Remove-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
Confirm
Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="9637f-111">Esse comando Remove o serviço vinculado denominado LinkedServiceTest do data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="9637f-111">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="9637f-112">Esse comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="9637f-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="9637f-113">OS</span><span class="sxs-lookup"><span data-stu-id="9637f-113">PARAMETERS</span></span>

### <span data-ttu-id="9637f-114">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="9637f-114">-DataFactory</span></span>
<span data-ttu-id="9637f-115">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="9637f-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="9637f-116">Esse cmdlet Remove um serviço vinculado do alocador de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="9637f-116">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9637f-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="9637f-117">-DataFactoryName</span></span>
<span data-ttu-id="9637f-118">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="9637f-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="9637f-119">Esse cmdlet Remove um serviço vinculado do alocador de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="9637f-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9637f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9637f-120">-DefaultProfile</span></span>
<span data-ttu-id="9637f-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="9637f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9637f-122">-Force</span><span class="sxs-lookup"><span data-stu-id="9637f-122">-Force</span></span>
<span data-ttu-id="9637f-123">Indica que esse cmdlet Remove um serviço vinculado sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="9637f-123">Indicates that this cmdlet removes a linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="9637f-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="9637f-124">-Name</span></span>
<span data-ttu-id="9637f-125">Especifica o nome do serviço vinculado a ser removido.</span><span class="sxs-lookup"><span data-stu-id="9637f-125">Specifies the name of the linked service to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9637f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9637f-126">-ResourceGroupName</span></span>
<span data-ttu-id="9637f-127">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="9637f-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="9637f-128">Esse cmdlet Remove um serviço vinculado do grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="9637f-128">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9637f-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9637f-129">-Confirm</span></span>
<span data-ttu-id="9637f-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9637f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9637f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9637f-131">-WhatIf</span></span>
<span data-ttu-id="9637f-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9637f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9637f-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9637f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9637f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9637f-134">CommonParameters</span></span>
<span data-ttu-id="9637f-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9637f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9637f-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9637f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9637f-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9637f-137">INPUTS</span></span>

### <span data-ttu-id="9637f-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="9637f-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="9637f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9637f-139">System.String</span></span>

## <span data-ttu-id="9637f-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9637f-140">OUTPUTS</span></span>

### <span data-ttu-id="9637f-141">System. void</span><span class="sxs-lookup"><span data-stu-id="9637f-141">System.Void</span></span>

## <span data-ttu-id="9637f-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9637f-142">NOTES</span></span>
* <span data-ttu-id="9637f-143">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="9637f-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="9637f-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9637f-144">RELATED LINKS</span></span>

[<span data-ttu-id="9637f-145">Get-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="9637f-145">Get-AzureRmDataFactoryLinkedService</span></span>](./Get-AzureRmDataFactoryLinkedService.md)

[<span data-ttu-id="9637f-146">New-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="9637f-146">New-AzureRmDataFactoryLinkedService</span></span>](./New-AzureRmDataFactoryLinkedService.md)


