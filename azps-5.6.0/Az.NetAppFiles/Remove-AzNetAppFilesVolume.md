---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
ms.openlocfilehash: f53ca76da23620a37020a14877059aae4f4c9808
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887419"
---
# <span data-ttu-id="ae079-101">Remove-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="ae079-101">Remove-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="ae079-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae079-102">SYNOPSIS</span></span>
<span data-ttu-id="ae079-103">Exclui um volume Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="ae079-103">Deletes an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="ae079-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ae079-104">SYNTAX</span></span>

### <span data-ttu-id="ae079-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ae079-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae079-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae079-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae079-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae079-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae079-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae079-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae079-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ae079-109">DESCRIPTION</span></span>
<span data-ttu-id="ae079-110">O cmdlet **Remove-AzNetAppFilesVolume** exclui um volume ANF.</span><span class="sxs-lookup"><span data-stu-id="ae079-110">The **Remove-AzNetAppFilesVolume** cmdlet deletes an ANF volume.</span></span>

## <span data-ttu-id="ae079-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae079-111">EXAMPLES</span></span>

### <span data-ttu-id="ae079-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ae079-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"
```

<span data-ttu-id="ae079-113">Este comando exclui o volume da ANF "MyAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="ae079-113">This command deletes the ANF volume "MyAnfVolume".</span></span>

## <span data-ttu-id="ae079-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ae079-114">PARAMETERS</span></span>

### <span data-ttu-id="ae079-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ae079-115">-AccountName</span></span>
<span data-ttu-id="ae079-116">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="ae079-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="ae079-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae079-117">-DefaultProfile</span></span>
<span data-ttu-id="ae079-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ae079-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae079-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae079-119">-InputObject</span></span>
<span data-ttu-id="ae079-120">O objeto volume a ser removido</span><span class="sxs-lookup"><span data-stu-id="ae079-120">The volume object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae079-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ae079-121">-Name</span></span>
<span data-ttu-id="ae079-122">O nome do volume da ANF</span><span class="sxs-lookup"><span data-stu-id="ae079-122">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae079-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae079-123">-PassThru</span></span>
<span data-ttu-id="ae079-124">Retornar se o volume especificado foi removido com êxito</span><span class="sxs-lookup"><span data-stu-id="ae079-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="ae079-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="ae079-125">-PoolName</span></span>
<span data-ttu-id="ae079-126">O nome do pool ANF</span><span class="sxs-lookup"><span data-stu-id="ae079-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="ae079-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="ae079-127">-PoolObject</span></span>
<span data-ttu-id="ae079-128">O objeto pool que contém o volume a ser removido</span><span class="sxs-lookup"><span data-stu-id="ae079-128">The pool object containing the volume to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae079-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae079-129">-ResourceGroupName</span></span>
<span data-ttu-id="ae079-130">O grupo de recursos do volume ANF</span><span class="sxs-lookup"><span data-stu-id="ae079-130">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="ae079-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae079-131">-ResourceId</span></span>
<span data-ttu-id="ae079-132">A id de recurso do volume ANF</span><span class="sxs-lookup"><span data-stu-id="ae079-132">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="ae079-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae079-133">-Confirm</span></span>
<span data-ttu-id="ae079-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae079-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae079-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae079-135">-WhatIf</span></span>
<span data-ttu-id="ae079-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ae079-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae079-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ae079-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae079-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae079-138">CommonParameters</span></span>
<span data-ttu-id="ae079-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae079-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae079-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae079-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae079-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ae079-141">INPUTS</span></span>

### <span data-ttu-id="ae079-142">System.String</span><span class="sxs-lookup"><span data-stu-id="ae079-142">System.String</span></span>

### <span data-ttu-id="ae079-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="ae079-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="ae079-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="ae079-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="ae079-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ae079-145">OUTPUTS</span></span>

### <span data-ttu-id="ae079-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ae079-146">System.Boolean</span></span>

## <span data-ttu-id="ae079-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="ae079-147">NOTES</span></span>

## <span data-ttu-id="ae079-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae079-148">RELATED LINKS</span></span>
