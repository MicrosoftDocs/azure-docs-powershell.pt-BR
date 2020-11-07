---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2.md
ms.openlocfilehash: c396455804f6bb501fa6439fceffb0eb45875516
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940473"
---
# <span data-ttu-id="1eece-101">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="1eece-101">Remove-AzDataFactoryV2</span></span>

## <span data-ttu-id="1eece-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1eece-102">SYNOPSIS</span></span>
<span data-ttu-id="1eece-103">Remove uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="1eece-103">Removes a data factory.</span></span>

## <span data-ttu-id="1eece-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1eece-104">SYNTAX</span></span>

### <span data-ttu-id="1eece-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="1eece-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1eece-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1eece-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryV2 [-InputObject] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1eece-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1eece-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2 [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1eece-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1eece-108">DESCRIPTION</span></span>
<span data-ttu-id="1eece-109">O cmdlet Remove-AzDataFactoryV2 remove uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="1eece-109">The Remove-AzDataFactoryV2 cmdlet removes a data factory.</span></span>

## <span data-ttu-id="1eece-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1eece-110">EXAMPLES</span></span>

### <span data-ttu-id="1eece-111">Exemplo 1: remover uma fábrica de dados</span><span class="sxs-lookup"><span data-stu-id="1eece-111">Example 1: Remove a data factory</span></span>
```
PS C:\> Remove-AzDataFactoryV2 -Name "WikiADF" -ResourceGroupName "ADF"
          Confirm
          Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="1eece-112">Esse comando Remove a fábrica de dados chamada WikiADF do grupo de recursos chamado ADF.</span><span class="sxs-lookup"><span data-stu-id="1eece-112">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="1eece-113">Esse comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="1eece-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="1eece-114">OS</span><span class="sxs-lookup"><span data-stu-id="1eece-114">PARAMETERS</span></span>

### <span data-ttu-id="1eece-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1eece-115">-DefaultProfile</span></span>
<span data-ttu-id="1eece-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1eece-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1eece-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1eece-117">-Force</span></span>
<span data-ttu-id="1eece-118">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="1eece-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="1eece-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1eece-119">-InputObject</span></span>
<span data-ttu-id="1eece-120">Especifica o objeto datafactory a ser removido.</span><span class="sxs-lookup"><span data-stu-id="1eece-120">Specifies the DataFactory object to remove.</span></span>

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

### <span data-ttu-id="1eece-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="1eece-121">-Name</span></span>
<span data-ttu-id="1eece-122">Especifica o nome da fábrica de dados a ser removida.</span><span class="sxs-lookup"><span data-stu-id="1eece-122">Specifies the name of the data factory to remove.</span></span>

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

### <span data-ttu-id="1eece-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1eece-123">-ResourceGroupName</span></span>
<span data-ttu-id="1eece-124">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="1eece-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1eece-125">Esse cmdlet Remove uma fábrica de dados do grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="1eece-125">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1eece-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1eece-126">-ResourceId</span></span>
<span data-ttu-id="1eece-127">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="1eece-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="1eece-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1eece-128">-Confirm</span></span>
<span data-ttu-id="1eece-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1eece-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1eece-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1eece-130">-WhatIf</span></span>
<span data-ttu-id="1eece-131">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1eece-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="1eece-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eece-132">CommonParameters</span></span>
<span data-ttu-id="1eece-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1eece-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eece-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1eece-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eece-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1eece-135">INPUTS</span></span>

### <span data-ttu-id="1eece-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1eece-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="1eece-137">System. String</span><span class="sxs-lookup"><span data-stu-id="1eece-137">System.String</span></span>

## <span data-ttu-id="1eece-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1eece-138">OUTPUTS</span></span>

### <span data-ttu-id="1eece-139">System. void</span><span class="sxs-lookup"><span data-stu-id="1eece-139">System.Void</span></span>

## <span data-ttu-id="1eece-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1eece-140">NOTES</span></span>
<span data-ttu-id="1eece-141">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="1eece-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1eece-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1eece-142">RELATED LINKS</span></span>

[<span data-ttu-id="1eece-143">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="1eece-143">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="1eece-144">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="1eece-144">Set-AzDataFactoryV2</span></span>]()
