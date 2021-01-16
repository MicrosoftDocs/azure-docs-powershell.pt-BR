---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/set-aznetAppfilesvolumepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesVolumePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesVolumePool.md
ms.openlocfilehash: 30d525ebcb7d80a24e11080ee265eb509f575ff6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271936"
---
# <span data-ttu-id="c38c6-101">Set-AzNetAppFilesVolumePool</span><span class="sxs-lookup"><span data-stu-id="c38c6-101">Set-AzNetAppFilesVolumePool</span></span>

## <span data-ttu-id="c38c6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c38c6-102">SYNOPSIS</span></span>
<span data-ttu-id="c38c6-103">Alterar o pool para um volume de arquivos do Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="c38c6-103">Change pool for an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="c38c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c38c6-104">SYNTAX</span></span>

### <span data-ttu-id="c38c6-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c38c6-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzNetAppFilesVolumePool -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-NewPoolResourceId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c38c6-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c38c6-106">ByParentObjectParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -Name <String> -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c38c6-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c38c6-107">ByResourceIdParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c38c6-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c38c6-108">ByObjectParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -InputObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c38c6-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c38c6-109">DESCRIPTION</span></span>
<span data-ttu-id="c38c6-110">O cmdlet **set-AzNetAppFilesVolumePool** altera o pool de um volume ANF.</span><span class="sxs-lookup"><span data-stu-id="c38c6-110">The **Set-AzNetAppFilesVolumePool** cmdlet changes the pool of an ANF volume.</span></span>

## <span data-ttu-id="c38c6-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c38c6-111">EXAMPLES</span></span>

### <span data-ttu-id="c38c6-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c38c6-112">Example 1</span></span>
```powershell
PS C:\>Set-AzNetAppFilesVolumePool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -NewPoolResourceId 7d6e4069-6c78-6c61-7bf6-c60968e45fbf
```

<span data-ttu-id="c38c6-113">Isso altera o pool do volume myvolume para um com a ID de 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span><span class="sxs-lookup"><span data-stu-id="c38c6-113">This changes the pool for the volume MyVolume to one with the Id of 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span></span>

## <span data-ttu-id="c38c6-114">OS</span><span class="sxs-lookup"><span data-stu-id="c38c6-114">PARAMETERS</span></span>

### <span data-ttu-id="c38c6-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c38c6-115">-AccountName</span></span>
<span data-ttu-id="c38c6-116">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="c38c6-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="c38c6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c38c6-117">-DefaultProfile</span></span>
<span data-ttu-id="c38c6-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c38c6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c38c6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c38c6-119">-InputObject</span></span>
<span data-ttu-id="c38c6-120">O objeto volume para mover</span><span class="sxs-lookup"><span data-stu-id="c38c6-120">The volume object to move</span></span>

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

### <span data-ttu-id="c38c6-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="c38c6-121">-Name</span></span>
<span data-ttu-id="c38c6-122">O nome do volume ANF</span><span class="sxs-lookup"><span data-stu-id="c38c6-122">The name of the ANF volume</span></span>

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

### <span data-ttu-id="c38c6-123">-NewPoolResourceId</span><span class="sxs-lookup"><span data-stu-id="c38c6-123">-NewPoolResourceId</span></span>
<span data-ttu-id="c38c6-124">ResourceId do pool de capacidade para o qual mover.</span><span class="sxs-lookup"><span data-stu-id="c38c6-124">ResourceId of the capacity pool to move to.</span></span>
<span data-ttu-id="c38c6-125">UUID v4 usado para identificar o pool</span><span class="sxs-lookup"><span data-stu-id="c38c6-125">UUID v4 used to identify the pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c38c6-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="c38c6-126">-PoolName</span></span>
<span data-ttu-id="c38c6-127">O nome do pool ANF</span><span class="sxs-lookup"><span data-stu-id="c38c6-127">The name of the ANF pool</span></span>

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

### <span data-ttu-id="c38c6-128">-Poolobject</span><span class="sxs-lookup"><span data-stu-id="c38c6-128">-PoolObject</span></span>
<span data-ttu-id="c38c6-129">O objeto de pool que contém o volume</span><span class="sxs-lookup"><span data-stu-id="c38c6-129">The pool object containing the volume</span></span>

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

### <span data-ttu-id="c38c6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c38c6-130">-ResourceGroupName</span></span>
<span data-ttu-id="c38c6-131">O grupo de recursos do volume ANF</span><span class="sxs-lookup"><span data-stu-id="c38c6-131">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="c38c6-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c38c6-132">-ResourceId</span></span>
<span data-ttu-id="c38c6-133">A ID do recurso do volume ANF</span><span class="sxs-lookup"><span data-stu-id="c38c6-133">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="c38c6-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c38c6-134">-Confirm</span></span>
<span data-ttu-id="c38c6-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c38c6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c38c6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c38c6-136">-WhatIf</span></span>
<span data-ttu-id="c38c6-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c38c6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c38c6-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c38c6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c38c6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c38c6-139">CommonParameters</span></span>
<span data-ttu-id="c38c6-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c38c6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c38c6-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c38c6-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c38c6-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c38c6-142">INPUTS</span></span>

### <span data-ttu-id="c38c6-143">System. String</span><span class="sxs-lookup"><span data-stu-id="c38c6-143">System.String</span></span>

### <span data-ttu-id="c38c6-144">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="c38c6-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="c38c6-145">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="c38c6-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="c38c6-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c38c6-146">OUTPUTS</span></span>

### <span data-ttu-id="c38c6-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c38c6-147">System.Boolean</span></span>

## <span data-ttu-id="c38c6-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c38c6-148">NOTES</span></span>

## <span data-ttu-id="c38c6-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c38c6-149">RELATED LINKS</span></span>
