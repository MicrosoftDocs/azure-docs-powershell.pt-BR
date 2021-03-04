---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
ms.openlocfilehash: a62e6093ec5cfdf7244ea83b2dccf07ad07308fb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887426"
---
# <span data-ttu-id="9c374-101">Remove-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="9c374-101">Remove-AzNetAppFilesPool</span></span>

## <span data-ttu-id="9c374-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c374-102">SYNOPSIS</span></span>
<span data-ttu-id="9c374-103">Exclui um pool de Arquivos do Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="9c374-103">Deletes an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="9c374-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9c374-104">SYNTAX</span></span>

### <span data-ttu-id="9c374-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9c374-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c374-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c374-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c374-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c374-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesPool -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c374-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c374-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -InputObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c374-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9c374-109">DESCRIPTION</span></span>
<span data-ttu-id="9c374-110">O cmdlet **Remove-AzNetAppFilesPool** exclui um pool ANF.</span><span class="sxs-lookup"><span data-stu-id="9c374-110">The **Remove-AzNetAppFilesPool** cmdlet deletes an ANF pool.</span></span>

## <span data-ttu-id="9c374-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c374-111">EXAMPLES</span></span>

### <span data-ttu-id="9c374-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9c374-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool"
```

<span data-ttu-id="9c374-113">Este comando exclui o pool ANF "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="9c374-113">This command deletes the ANF pool "MyAnfPool".</span></span>

## <span data-ttu-id="9c374-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9c374-114">PARAMETERS</span></span>

### <span data-ttu-id="9c374-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9c374-115">-AccountName</span></span>
<span data-ttu-id="9c374-116">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="9c374-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c374-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="9c374-117">-AccountObject</span></span>
<span data-ttu-id="9c374-118">O objeto account que contém o pool a ser removido</span><span class="sxs-lookup"><span data-stu-id="9c374-118">The account object containing the pool to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c374-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c374-119">-DefaultProfile</span></span>
<span data-ttu-id="9c374-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9c374-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c374-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c374-121">-InputObject</span></span>
<span data-ttu-id="9c374-122">O objeto pool a ser removido</span><span class="sxs-lookup"><span data-stu-id="9c374-122">The pool object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c374-123">-Name</span><span class="sxs-lookup"><span data-stu-id="9c374-123">-Name</span></span>
<span data-ttu-id="9c374-124">O nome do pool ANF</span><span class="sxs-lookup"><span data-stu-id="9c374-124">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c374-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c374-125">-PassThru</span></span>
<span data-ttu-id="9c374-126">Retornar se o pool especificado foi removido com êxito</span><span class="sxs-lookup"><span data-stu-id="9c374-126">Return whether the specified pool was successfully removed</span></span>

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

### <span data-ttu-id="9c374-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c374-127">-ResourceGroupName</span></span>
<span data-ttu-id="9c374-128">O grupo de recursos do pool ANF</span><span class="sxs-lookup"><span data-stu-id="9c374-128">The resource group of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c374-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c374-129">-ResourceId</span></span>
<span data-ttu-id="9c374-130">A id de recurso do pool de ANF</span><span class="sxs-lookup"><span data-stu-id="9c374-130">The resource id of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c374-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c374-131">-Confirm</span></span>
<span data-ttu-id="9c374-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c374-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c374-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c374-133">-WhatIf</span></span>
<span data-ttu-id="9c374-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9c374-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c374-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9c374-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c374-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c374-136">CommonParameters</span></span>
<span data-ttu-id="9c374-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c374-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c374-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c374-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c374-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9c374-139">INPUTS</span></span>

### <span data-ttu-id="9c374-140">System.String</span><span class="sxs-lookup"><span data-stu-id="9c374-140">System.String</span></span>

### <span data-ttu-id="9c374-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="9c374-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="9c374-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="9c374-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="9c374-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9c374-143">OUTPUTS</span></span>

### <span data-ttu-id="9c374-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9c374-144">System.Boolean</span></span>

## <span data-ttu-id="9c374-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="9c374-145">NOTES</span></span>

## <span data-ttu-id="9c374-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c374-146">RELATED LINKS</span></span>
