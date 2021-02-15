---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesPool.md
ms.openlocfilehash: 1ab6d38cc5401b4a7e813dafac933d6601a75acd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114221"
---
# <span data-ttu-id="62208-101">Remove-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="62208-101">Remove-AzNetAppFilesPool</span></span>

## <span data-ttu-id="62208-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="62208-102">SYNOPSIS</span></span>
<span data-ttu-id="62208-103">Exclui um pool de Arquivos Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="62208-103">Deletes an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="62208-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="62208-104">SYNTAX</span></span>

### <span data-ttu-id="62208-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="62208-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62208-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="62208-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62208-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="62208-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesPool -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62208-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="62208-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesPool -InputObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62208-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="62208-109">DESCRIPTION</span></span>
<span data-ttu-id="62208-110">O **cmdlet Remove-AzNetAppFilesPool** exclui um pool ANF.</span><span class="sxs-lookup"><span data-stu-id="62208-110">The **Remove-AzNetAppFilesPool** cmdlet deletes an ANF pool.</span></span>

## <span data-ttu-id="62208-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="62208-111">EXAMPLES</span></span>

### <span data-ttu-id="62208-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="62208-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool"
```

<span data-ttu-id="62208-113">Esse comando exclui o pool de ANF "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="62208-113">This command deletes the ANF pool "MyAnfPool".</span></span>

## <span data-ttu-id="62208-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="62208-114">PARAMETERS</span></span>

### <span data-ttu-id="62208-115">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="62208-115">-AccountName</span></span>
<span data-ttu-id="62208-116">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="62208-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="62208-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="62208-117">-AccountObject</span></span>
<span data-ttu-id="62208-118">O objeto da conta que contém o pool a ser removido</span><span class="sxs-lookup"><span data-stu-id="62208-118">The account object containing the pool to remove</span></span>

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

### <span data-ttu-id="62208-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62208-119">-DefaultProfile</span></span>
<span data-ttu-id="62208-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="62208-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62208-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62208-121">-InputObject</span></span>
<span data-ttu-id="62208-122">O objeto de pool a ser removido</span><span class="sxs-lookup"><span data-stu-id="62208-122">The pool object to remove</span></span>

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

### <span data-ttu-id="62208-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="62208-123">-Name</span></span>
<span data-ttu-id="62208-124">O nome do pool de ANF</span><span class="sxs-lookup"><span data-stu-id="62208-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="62208-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62208-125">-PassThru</span></span>
<span data-ttu-id="62208-126">Retornar se o pool especificado foi removido com êxito</span><span class="sxs-lookup"><span data-stu-id="62208-126">Return whether the specified pool was successfully removed</span></span>

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

### <span data-ttu-id="62208-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62208-127">-ResourceGroupName</span></span>
<span data-ttu-id="62208-128">O grupo de recursos do pool de ANF</span><span class="sxs-lookup"><span data-stu-id="62208-128">The resource group of the ANF pool</span></span>

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

### <span data-ttu-id="62208-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62208-129">-ResourceId</span></span>
<span data-ttu-id="62208-130">A ID do recurso do pool de ANF</span><span class="sxs-lookup"><span data-stu-id="62208-130">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="62208-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="62208-131">-Confirm</span></span>
<span data-ttu-id="62208-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62208-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62208-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62208-133">-WhatIf</span></span>
<span data-ttu-id="62208-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="62208-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62208-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="62208-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62208-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62208-136">CommonParameters</span></span>
<span data-ttu-id="62208-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62208-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62208-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62208-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62208-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="62208-139">INPUTS</span></span>

### <span data-ttu-id="62208-140">System.String</span><span class="sxs-lookup"><span data-stu-id="62208-140">System.String</span></span>

### <span data-ttu-id="62208-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="62208-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="62208-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="62208-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="62208-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="62208-143">OUTPUTS</span></span>

### <span data-ttu-id="62208-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="62208-144">System.Boolean</span></span>

## <span data-ttu-id="62208-145">Notas</span><span class="sxs-lookup"><span data-stu-id="62208-145">NOTES</span></span>

## <span data-ttu-id="62208-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="62208-146">RELATED LINKS</span></span>
