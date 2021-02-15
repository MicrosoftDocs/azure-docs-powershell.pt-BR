---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 3D2E9FAE-FE34-457A-BE95-BC61D025B07A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactory.md
ms.openlocfilehash: 36c22a432d4e281600a1b718c1ac58a851fb7069
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111974"
---
# <span data-ttu-id="386b5-101">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="386b5-101">Remove-AzDataFactory</span></span>

## <span data-ttu-id="386b5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="386b5-102">SYNOPSIS</span></span>
<span data-ttu-id="386b5-103">Remove uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="386b5-103">Removes a data factory.</span></span>

## <span data-ttu-id="386b5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="386b5-104">SYNTAX</span></span>

### <span data-ttu-id="386b5-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="386b5-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactory [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="386b5-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="386b5-106">ByFactoryObject</span></span>
```
Remove-AzDataFactory [-DataFactory] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="386b5-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="386b5-107">DESCRIPTION</span></span>
<span data-ttu-id="386b5-108">O **cmdlet Remove-AzDataFactory** remove uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="386b5-108">The **Remove-AzDataFactory** cmdlet removes a data factory.</span></span>

## <span data-ttu-id="386b5-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="386b5-109">EXAMPLES</span></span>

### <span data-ttu-id="386b5-110">Exemplo 1: Remover uma fábrica de dados</span><span class="sxs-lookup"><span data-stu-id="386b5-110">Example 1: Remove a data factory</span></span>
```
PS C:\>Remove-AzDataFactory -Name "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="386b5-111">Esse comando remove a fábrica de dados chamada WikiADF do grupo de recursos chamado ADF.</span><span class="sxs-lookup"><span data-stu-id="386b5-111">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="386b5-112">Esse comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="386b5-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="386b5-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="386b5-113">PARAMETERS</span></span>

### <span data-ttu-id="386b5-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="386b5-114">-DataFactory</span></span>
<span data-ttu-id="386b5-115">Especifica o **objeto PSDataFactory a** ser removido.</span><span class="sxs-lookup"><span data-stu-id="386b5-115">Specifies the **PSDataFactory** object to remove.</span></span>

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

### <span data-ttu-id="386b5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="386b5-116">-DefaultProfile</span></span>
<span data-ttu-id="386b5-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="386b5-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="386b5-118">-Forçar</span><span class="sxs-lookup"><span data-stu-id="386b5-118">-Force</span></span>
<span data-ttu-id="386b5-119">Indica que esse cmdlet remove uma fábrica de dados sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="386b5-119">Indicates that this cmdlet removes a data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="386b5-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="386b5-120">-Name</span></span>
<span data-ttu-id="386b5-121">Especifica o nome da fábrica de dados a ser removido.</span><span class="sxs-lookup"><span data-stu-id="386b5-121">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="386b5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="386b5-122">-ResourceGroupName</span></span>
<span data-ttu-id="386b5-123">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="386b5-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="386b5-124">Este cmdlet remove uma fábrica de dados do grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="386b5-124">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="386b5-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="386b5-125">-Confirm</span></span>
<span data-ttu-id="386b5-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="386b5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="386b5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="386b5-127">-WhatIf</span></span>
<span data-ttu-id="386b5-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="386b5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="386b5-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="386b5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="386b5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="386b5-130">CommonParameters</span></span>
<span data-ttu-id="386b5-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="386b5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="386b5-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="386b5-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="386b5-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="386b5-133">INPUTS</span></span>

### <span data-ttu-id="386b5-134">System.String</span><span class="sxs-lookup"><span data-stu-id="386b5-134">System.String</span></span>

### <span data-ttu-id="386b5-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="386b5-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="386b5-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="386b5-136">OUTPUTS</span></span>

### <span data-ttu-id="386b5-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="386b5-137">System.Void</span></span>

## <span data-ttu-id="386b5-138">Notas</span><span class="sxs-lookup"><span data-stu-id="386b5-138">NOTES</span></span>
* <span data-ttu-id="386b5-139">Palavras-chave: azure, azurerm, arm, resource, management, manager, data,</span><span class="sxs-lookup"><span data-stu-id="386b5-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="386b5-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="386b5-140">RELATED LINKS</span></span>

[<span data-ttu-id="386b5-141">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="386b5-141">Get-AzDataFactory</span></span>](./Get-AzDataFactory.md)

[<span data-ttu-id="386b5-142">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="386b5-142">New-AzDataFactory</span></span>](./New-AzDataFactory.md)


