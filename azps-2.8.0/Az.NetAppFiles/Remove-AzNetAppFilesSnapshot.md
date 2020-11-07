---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 16eb962245502338c7b12f6e5abf20a9bc04b83f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772130"
---
# <span data-ttu-id="7fb56-101">Remove-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="7fb56-101">Remove-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="7fb56-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7fb56-102">SYNOPSIS</span></span>
<span data-ttu-id="7fb56-103">Exclui um instantâneo do Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="7fb56-103">Deletes an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="7fb56-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7fb56-104">SYNTAX</span></span>

### <span data-ttu-id="7fb56-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7fb56-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fb56-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fb56-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fb56-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fb56-107">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -VolumeObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fb56-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fb56-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -InputObject <PSNetAppFilesSnapshot> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fb56-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7fb56-109">DESCRIPTION</span></span>
<span data-ttu-id="7fb56-110">O cmdlet **Remove-AzNetAppFilesSnapshot** exclui um instantâneo ANF.</span><span class="sxs-lookup"><span data-stu-id="7fb56-110">The **Remove-AzNetAppFilesSnapshot** cmdlet deletes an ANF snapshot.</span></span>

## <span data-ttu-id="7fb56-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7fb56-111">EXAMPLES</span></span>

### <span data-ttu-id="7fb56-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7fb56-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -Name "MyAnfSnapshot"
```

<span data-ttu-id="7fb56-113">Esse comando exclui o instantâneo ANF "MyAnfSnapshot".</span><span class="sxs-lookup"><span data-stu-id="7fb56-113">This command deletes the ANF snapshot "MyAnfSnapshot".</span></span>

## <span data-ttu-id="7fb56-114">OS</span><span class="sxs-lookup"><span data-stu-id="7fb56-114">PARAMETERS</span></span>

### <span data-ttu-id="7fb56-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7fb56-115">-AccountName</span></span>
<span data-ttu-id="7fb56-116">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="7fb56-116">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fb56-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fb56-117">-DefaultProfile</span></span>
<span data-ttu-id="7fb56-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7fb56-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fb56-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7fb56-119">-InputObject</span></span>
<span data-ttu-id="7fb56-120">O objeto de instantâneo a ser removido</span><span class="sxs-lookup"><span data-stu-id="7fb56-120">The snapshot object to remove</span></span>

```yaml
Type: PSNetAppFilesSnapshot
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fb56-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="7fb56-121">-Name</span></span>
<span data-ttu-id="7fb56-122">O nome do instantâneo ANF</span><span class="sxs-lookup"><span data-stu-id="7fb56-122">The name of the ANF snapshot</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: SnapshotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fb56-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7fb56-123">-PassThru</span></span>
<span data-ttu-id="7fb56-124">Retornar se o volume especificado foi removido com êxito</span><span class="sxs-lookup"><span data-stu-id="7fb56-124">Return whether the specified volume was successfully removed</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fb56-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="7fb56-125">-PoolName</span></span>
<span data-ttu-id="7fb56-126">O nome do pool ANF</span><span class="sxs-lookup"><span data-stu-id="7fb56-126">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fb56-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fb56-127">-ResourceGroupName</span></span>
<span data-ttu-id="7fb56-128">O grupo de recursos do instantâneo ANF</span><span class="sxs-lookup"><span data-stu-id="7fb56-128">The resource group of the ANF snapshot</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fb56-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7fb56-129">-ResourceId</span></span>
<span data-ttu-id="7fb56-130">A ID do recurso do instantâneo ANF</span><span class="sxs-lookup"><span data-stu-id="7fb56-130">The resource id of the ANF snapshot</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fb56-131">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="7fb56-131">-VolumeName</span></span>
<span data-ttu-id="7fb56-132">O nome do volume ANF</span><span class="sxs-lookup"><span data-stu-id="7fb56-132">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fb56-133">-Volumeobject</span><span class="sxs-lookup"><span data-stu-id="7fb56-133">-VolumeObject</span></span>
<span data-ttu-id="7fb56-134">O objeto volume que contém o instantâneo a ser removido</span><span class="sxs-lookup"><span data-stu-id="7fb56-134">The volume object containing the snapshot to remove</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fb56-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7fb56-135">-Confirm</span></span>
<span data-ttu-id="7fb56-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7fb56-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fb56-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fb56-137">-WhatIf</span></span>
<span data-ttu-id="7fb56-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7fb56-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fb56-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7fb56-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fb56-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fb56-140">CommonParameters</span></span>
<span data-ttu-id="7fb56-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fb56-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7fb56-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fb56-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fb56-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7fb56-143">INPUTS</span></span>

### <span data-ttu-id="7fb56-144">System. String</span><span class="sxs-lookup"><span data-stu-id="7fb56-144">System.String</span></span>

### <span data-ttu-id="7fb56-145">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="7fb56-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="7fb56-146">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="7fb56-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="7fb56-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7fb56-147">OUTPUTS</span></span>

### <span data-ttu-id="7fb56-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7fb56-148">System.Boolean</span></span>

## <span data-ttu-id="7fb56-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7fb56-149">NOTES</span></span>

## <span data-ttu-id="7fb56-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7fb56-150">RELATED LINKS</span></span>
