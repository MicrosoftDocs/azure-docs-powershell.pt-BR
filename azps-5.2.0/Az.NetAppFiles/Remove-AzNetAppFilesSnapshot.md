---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 1d28420e9457826f7c851eb0d3013f36de9edbc2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260246"
---
# <span data-ttu-id="43672-101">Remove-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="43672-101">Remove-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="43672-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="43672-102">SYNOPSIS</span></span>
<span data-ttu-id="43672-103">Exclui um instantâneo do Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="43672-103">Deletes an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="43672-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="43672-104">SYNTAX</span></span>

### <span data-ttu-id="43672-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="43672-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43672-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="43672-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43672-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43672-107">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -VolumeObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43672-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43672-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -InputObject <PSNetAppFilesSnapshot> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43672-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="43672-109">DESCRIPTION</span></span>
<span data-ttu-id="43672-110">O cmdlet **Remove-AzNetAppFilesSnapshot** exclui um instantâneo ANF.</span><span class="sxs-lookup"><span data-stu-id="43672-110">The **Remove-AzNetAppFilesSnapshot** cmdlet deletes an ANF snapshot.</span></span>

## <span data-ttu-id="43672-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="43672-111">EXAMPLES</span></span>

### <span data-ttu-id="43672-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="43672-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -Name "MyAnfSnapshot"
```

<span data-ttu-id="43672-113">Esse comando exclui o instantâneo ANF "MyAnfSnapshot".</span><span class="sxs-lookup"><span data-stu-id="43672-113">This command deletes the ANF snapshot "MyAnfSnapshot".</span></span>

## <span data-ttu-id="43672-114">OS</span><span class="sxs-lookup"><span data-stu-id="43672-114">PARAMETERS</span></span>

### <span data-ttu-id="43672-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="43672-115">-AccountName</span></span>
<span data-ttu-id="43672-116">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="43672-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="43672-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43672-117">-DefaultProfile</span></span>
<span data-ttu-id="43672-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="43672-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43672-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43672-119">-InputObject</span></span>
<span data-ttu-id="43672-120">O objeto de instantâneo a ser removido</span><span class="sxs-lookup"><span data-stu-id="43672-120">The snapshot object to remove</span></span>

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

### <span data-ttu-id="43672-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="43672-121">-Name</span></span>
<span data-ttu-id="43672-122">O nome do instantâneo ANF</span><span class="sxs-lookup"><span data-stu-id="43672-122">The name of the ANF snapshot</span></span>

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

### <span data-ttu-id="43672-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43672-123">-PassThru</span></span>
<span data-ttu-id="43672-124">Retornar se o volume especificado foi removido com êxito</span><span class="sxs-lookup"><span data-stu-id="43672-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="43672-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="43672-125">-PoolName</span></span>
<span data-ttu-id="43672-126">O nome do pool ANF</span><span class="sxs-lookup"><span data-stu-id="43672-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="43672-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43672-127">-ResourceGroupName</span></span>
<span data-ttu-id="43672-128">O grupo de recursos do instantâneo ANF</span><span class="sxs-lookup"><span data-stu-id="43672-128">The resource group of the ANF snapshot</span></span>

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

### <span data-ttu-id="43672-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43672-129">-ResourceId</span></span>
<span data-ttu-id="43672-130">A ID do recurso do instantâneo ANF</span><span class="sxs-lookup"><span data-stu-id="43672-130">The resource id of the ANF snapshot</span></span>

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

### <span data-ttu-id="43672-131">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="43672-131">-VolumeName</span></span>
<span data-ttu-id="43672-132">O nome do volume ANF</span><span class="sxs-lookup"><span data-stu-id="43672-132">The name of the ANF volume</span></span>

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

### <span data-ttu-id="43672-133">-Volumeobject</span><span class="sxs-lookup"><span data-stu-id="43672-133">-VolumeObject</span></span>
<span data-ttu-id="43672-134">O objeto volume que contém o instantâneo a ser removido</span><span class="sxs-lookup"><span data-stu-id="43672-134">The volume object containing the snapshot to remove</span></span>

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

### <span data-ttu-id="43672-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="43672-135">-Confirm</span></span>
<span data-ttu-id="43672-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43672-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43672-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43672-137">-WhatIf</span></span>
<span data-ttu-id="43672-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="43672-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43672-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="43672-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43672-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43672-140">CommonParameters</span></span>
<span data-ttu-id="43672-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43672-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43672-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43672-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43672-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="43672-143">INPUTS</span></span>

### <span data-ttu-id="43672-144">System. String</span><span class="sxs-lookup"><span data-stu-id="43672-144">System.String</span></span>

### <span data-ttu-id="43672-145">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="43672-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="43672-146">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="43672-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="43672-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="43672-147">OUTPUTS</span></span>

### <span data-ttu-id="43672-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="43672-148">System.Boolean</span></span>

## <span data-ttu-id="43672-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="43672-149">NOTES</span></span>

## <span data-ttu-id="43672-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="43672-150">RELATED LINKS</span></span>
