---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 1d28420e9457826f7c851eb0d3013f36de9edbc2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112923"
---
# <span data-ttu-id="bd68a-101">Remove-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="bd68a-101">Remove-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="bd68a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bd68a-102">SYNOPSIS</span></span>
<span data-ttu-id="bd68a-103">Exclui um instantâneo do Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="bd68a-103">Deletes an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="bd68a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bd68a-104">SYNTAX</span></span>

### <span data-ttu-id="bd68a-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bd68a-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd68a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd68a-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd68a-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd68a-107">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -VolumeObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd68a-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd68a-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -InputObject <PSNetAppFilesSnapshot> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd68a-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="bd68a-109">DESCRIPTION</span></span>
<span data-ttu-id="bd68a-110">O cmdlet **Remove-AzNetAppFilesSnapshot** exclui um instantâneo ANF.</span><span class="sxs-lookup"><span data-stu-id="bd68a-110">The **Remove-AzNetAppFilesSnapshot** cmdlet deletes an ANF snapshot.</span></span>

## <span data-ttu-id="bd68a-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bd68a-111">EXAMPLES</span></span>

### <span data-ttu-id="bd68a-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bd68a-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -Name "MyAnfSnapshot"
```

<span data-ttu-id="bd68a-113">Esse comando exclui o instantâneo ANF "MyAnfSnapshot".</span><span class="sxs-lookup"><span data-stu-id="bd68a-113">This command deletes the ANF snapshot "MyAnfSnapshot".</span></span>

## <span data-ttu-id="bd68a-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bd68a-114">PARAMETERS</span></span>

### <span data-ttu-id="bd68a-115">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="bd68a-115">-AccountName</span></span>
<span data-ttu-id="bd68a-116">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="bd68a-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="bd68a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd68a-117">-DefaultProfile</span></span>
<span data-ttu-id="bd68a-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bd68a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd68a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd68a-119">-InputObject</span></span>
<span data-ttu-id="bd68a-120">O objeto instantâneo a ser removido</span><span class="sxs-lookup"><span data-stu-id="bd68a-120">The snapshot object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd68a-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="bd68a-121">-Name</span></span>
<span data-ttu-id="bd68a-122">O nome do instantâneo ANF</span><span class="sxs-lookup"><span data-stu-id="bd68a-122">The name of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: SnapshotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd68a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd68a-123">-PassThru</span></span>
<span data-ttu-id="bd68a-124">Retornar se o volume especificado foi removido com êxito</span><span class="sxs-lookup"><span data-stu-id="bd68a-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="bd68a-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="bd68a-125">-PoolName</span></span>
<span data-ttu-id="bd68a-126">O nome do pool de ANF</span><span class="sxs-lookup"><span data-stu-id="bd68a-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="bd68a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd68a-127">-ResourceGroupName</span></span>
<span data-ttu-id="bd68a-128">O grupo de recursos do instantâneo ANF</span><span class="sxs-lookup"><span data-stu-id="bd68a-128">The resource group of the ANF snapshot</span></span>

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

### <span data-ttu-id="bd68a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd68a-129">-ResourceId</span></span>
<span data-ttu-id="bd68a-130">A ID do recurso do instantâneo ANF</span><span class="sxs-lookup"><span data-stu-id="bd68a-130">The resource id of the ANF snapshot</span></span>

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

### <span data-ttu-id="bd68a-131">-Nomedo Volume</span><span class="sxs-lookup"><span data-stu-id="bd68a-131">-VolumeName</span></span>
<span data-ttu-id="bd68a-132">O nome do volume da ANF</span><span class="sxs-lookup"><span data-stu-id="bd68a-132">The name of the ANF volume</span></span>

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

### <span data-ttu-id="bd68a-133">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="bd68a-133">-VolumeObject</span></span>
<span data-ttu-id="bd68a-134">O objeto de volume que contém o instantâneo a ser removido</span><span class="sxs-lookup"><span data-stu-id="bd68a-134">The volume object containing the snapshot to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd68a-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="bd68a-135">-Confirm</span></span>
<span data-ttu-id="bd68a-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd68a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd68a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd68a-137">-WhatIf</span></span>
<span data-ttu-id="bd68a-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="bd68a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd68a-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bd68a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd68a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd68a-140">CommonParameters</span></span>
<span data-ttu-id="bd68a-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd68a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd68a-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd68a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd68a-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="bd68a-143">INPUTS</span></span>

### <span data-ttu-id="bd68a-144">System.String</span><span class="sxs-lookup"><span data-stu-id="bd68a-144">System.String</span></span>

### <span data-ttu-id="bd68a-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="bd68a-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="bd68a-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="bd68a-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="bd68a-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="bd68a-147">OUTPUTS</span></span>

### <span data-ttu-id="bd68a-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bd68a-148">System.Boolean</span></span>

## <span data-ttu-id="bd68a-149">Notas</span><span class="sxs-lookup"><span data-stu-id="bd68a-149">NOTES</span></span>

## <span data-ttu-id="bd68a-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bd68a-150">RELATED LINKS</span></span>
