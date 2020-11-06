---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
ms.openlocfilehash: bba4df58ed4046eeba562e3438119e1d5df40649
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431770"
---
# <span data-ttu-id="79b70-101">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="79b70-101">Remove-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="79b70-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="79b70-102">SYNOPSIS</span></span>
<span data-ttu-id="79b70-103">Remove um serviço vinculado da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="79b70-103">Removes a linked service from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79b70-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="79b70-104">SYNTAX</span></span>

### <span data-ttu-id="79b70-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="79b70-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="79b70-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="79b70-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-InputObject] <PSLinkedService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79b70-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="79b70-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79b70-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="79b70-108">DESCRIPTION</span></span>
<span data-ttu-id="79b70-109">O cmdlet Remove-AzureRmDataFactoryV2LinkedService remove um serviço vinculado do Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="79b70-109">The Remove-AzureRmDataFactoryV2LinkedService cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="79b70-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="79b70-110">EXAMPLES</span></span>

### <span data-ttu-id="79b70-111">Exemplo 1: remover um serviço vinculado</span><span class="sxs-lookup"><span data-stu-id="79b70-111">Example 1: Remove a linked service</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
          Confirm
          Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="79b70-112">Esse comando Remove o serviço vinculado denominado LinkedServiceTest do data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="79b70-112">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="79b70-113">Esse comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="79b70-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="79b70-114">OS</span><span class="sxs-lookup"><span data-stu-id="79b70-114">PARAMETERS</span></span>

### <span data-ttu-id="79b70-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="79b70-115">-Confirm</span></span>
<span data-ttu-id="79b70-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79b70-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79b70-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="79b70-117">-DataFactoryName</span></span>
<span data-ttu-id="79b70-118">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="79b70-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="79b70-119">Esse cmdlet Remove um serviço vinculado do alocador de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="79b70-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="79b70-120">-Force</span><span class="sxs-lookup"><span data-stu-id="79b70-120">-Force</span></span>
<span data-ttu-id="79b70-121">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="79b70-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="79b70-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79b70-122">-InputObject</span></span>
<span data-ttu-id="79b70-123">Especifica o objeto LinkedService a ser removido.</span><span class="sxs-lookup"><span data-stu-id="79b70-123">Specifies the LinkedService object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79b70-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="79b70-124">-Name</span></span>
<span data-ttu-id="79b70-125">Especifica o nome do serviço vinculado a ser removido.</span><span class="sxs-lookup"><span data-stu-id="79b70-125">Specifies the name of the linked service to remove.</span></span>
<span data-ttu-id="79b70-126">Nome do serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="79b70-126">Name of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79b70-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79b70-127">-ResourceGroupName</span></span>
<span data-ttu-id="79b70-128">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="79b70-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="79b70-129">Esse cmdlet Remove um serviço vinculado do grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="79b70-129">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>


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

### <span data-ttu-id="79b70-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79b70-130">-ResourceId</span></span>
<span data-ttu-id="79b70-131">A ID de recurso do Azure do serviço vinculado a ser removido.</span><span class="sxs-lookup"><span data-stu-id="79b70-131">The Azure resource ID of the linked service to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79b70-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79b70-132">-WhatIf</span></span>
<span data-ttu-id="79b70-133">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79b70-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79b70-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79b70-134">-DefaultProfile</span></span>
<span data-ttu-id="79b70-135">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="79b70-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79b70-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79b70-136">CommonParameters</span></span>
<span data-ttu-id="79b70-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79b70-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79b70-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79b70-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79b70-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="79b70-139">INPUTS</span></span>

### <span data-ttu-id="79b70-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="79b70-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>
<span data-ttu-id="79b70-141">System. String</span><span class="sxs-lookup"><span data-stu-id="79b70-141">System.String</span></span>

## <span data-ttu-id="79b70-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="79b70-142">OUTPUTS</span></span>

### <span data-ttu-id="79b70-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="79b70-143">System.Object</span></span>

## <span data-ttu-id="79b70-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="79b70-144">NOTES</span></span>
<span data-ttu-id="79b70-145">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="79b70-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="79b70-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="79b70-146">RELATED LINKS</span></span>

[<span data-ttu-id="79b70-147">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="79b70-147">Get-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="79b70-148">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="79b70-148">Set-AzureRmDataFactoryV2LinkedService</span></span>]()

