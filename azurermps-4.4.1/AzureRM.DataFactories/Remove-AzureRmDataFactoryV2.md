---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
ms.openlocfilehash: 9d7d3e3ae06d46b1ea3cb3b1e4e8db1944dc87e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431780"
---
# <span data-ttu-id="81862-101">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="81862-101">Remove-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="81862-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="81862-102">SYNOPSIS</span></span>
<span data-ttu-id="81862-103">Remove uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="81862-103">Removes a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81862-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81862-104">SYNTAX</span></span>

### <span data-ttu-id="81862-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="81862-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81862-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="81862-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryV2 [-InputObject] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81862-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="81862-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81862-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="81862-108">DESCRIPTION</span></span>
<span data-ttu-id="81862-109">O cmdlet Remove-AzureRmDataFactoryV2 remove uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="81862-109">The Remove-AzureRmDataFactoryV2 cmdlet removes a data factory.</span></span>

## <span data-ttu-id="81862-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81862-110">EXAMPLES</span></span>

### <span data-ttu-id="81862-111">Exemplo 1: remover uma fábrica de dados</span><span class="sxs-lookup"><span data-stu-id="81862-111">Example 1: Remove a data factory</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2 -Name "WikiADF" -ResourceGroupName "ADF"
          Confirm
          Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="81862-112">Esse comando Remove a fábrica de dados chamada WikiADF do grupo de recursos chamado ADF.</span><span class="sxs-lookup"><span data-stu-id="81862-112">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="81862-113">Esse comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="81862-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="81862-114">OS</span><span class="sxs-lookup"><span data-stu-id="81862-114">PARAMETERS</span></span>

### <span data-ttu-id="81862-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="81862-115">-Confirm</span></span>
<span data-ttu-id="81862-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81862-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81862-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81862-117">-InputObject</span></span>
<span data-ttu-id="81862-118">Especifica o objeto datafactory a ser removido.</span><span class="sxs-lookup"><span data-stu-id="81862-118">Specifies the DataFactory object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81862-119">-Force</span><span class="sxs-lookup"><span data-stu-id="81862-119">-Force</span></span>
<span data-ttu-id="81862-120">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="81862-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="81862-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="81862-121">-Name</span></span>
<span data-ttu-id="81862-122">Especifica o nome da fábrica de dados a ser removida.</span><span class="sxs-lookup"><span data-stu-id="81862-122">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81862-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81862-123">-ResourceGroupName</span></span>
<span data-ttu-id="81862-124">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="81862-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="81862-125">Esse cmdlet Remove uma fábrica de dados do grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="81862-125">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81862-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81862-126">-ResourceId</span></span>
<span data-ttu-id="81862-127">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="81862-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="81862-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81862-128">-WhatIf</span></span>
<span data-ttu-id="81862-129">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81862-129">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="81862-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81862-130">-DefaultProfile</span></span>
<span data-ttu-id="81862-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="81862-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81862-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81862-132">CommonParameters</span></span>
<span data-ttu-id="81862-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81862-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81862-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81862-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81862-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="81862-135">INPUTS</span></span>

### <span data-ttu-id="81862-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="81862-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="81862-137">System. String</span><span class="sxs-lookup"><span data-stu-id="81862-137">System.String</span></span>

## <span data-ttu-id="81862-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="81862-138">OUTPUTS</span></span>

### <span data-ttu-id="81862-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="81862-139">System.Object</span></span>

## <span data-ttu-id="81862-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="81862-140">NOTES</span></span>
<span data-ttu-id="81862-141">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="81862-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="81862-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81862-142">RELATED LINKS</span></span>

[<span data-ttu-id="81862-143">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="81862-143">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="81862-144">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="81862-144">Set-AzureRmDataFactoryV2</span></span>]()
