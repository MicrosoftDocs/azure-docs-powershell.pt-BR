---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/set-aznetAppfilesvolumepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesVolumePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesVolumePool.md
ms.openlocfilehash: 30d525ebcb7d80a24e11080ee265eb509f575ff6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114728"
---
# <span data-ttu-id="5db07-101">Set-AzNetAppFilesVolumePool</span><span class="sxs-lookup"><span data-stu-id="5db07-101">Set-AzNetAppFilesVolumePool</span></span>

## <span data-ttu-id="5db07-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5db07-102">SYNOPSIS</span></span>
<span data-ttu-id="5db07-103">Altere o pool para um volume de Arquivos Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="5db07-103">Change pool for an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="5db07-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5db07-104">SYNTAX</span></span>

### <span data-ttu-id="5db07-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5db07-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzNetAppFilesVolumePool -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-NewPoolResourceId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5db07-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5db07-106">ByParentObjectParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -Name <String> -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5db07-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5db07-107">ByResourceIdParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5db07-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5db07-108">ByObjectParameterSet</span></span>
```
Set-AzNetAppFilesVolumePool -InputObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5db07-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="5db07-109">DESCRIPTION</span></span>
<span data-ttu-id="5db07-110">O cmdlet **Set-AzNetAppFilesVolumePool** altera o pool de um volume ANF.</span><span class="sxs-lookup"><span data-stu-id="5db07-110">The **Set-AzNetAppFilesVolumePool** cmdlet changes the pool of an ANF volume.</span></span>

## <span data-ttu-id="5db07-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5db07-111">EXAMPLES</span></span>

### <span data-ttu-id="5db07-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5db07-112">Example 1</span></span>
```powershell
PS C:\>Set-AzNetAppFilesVolumePool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -NewPoolResourceId 7d6e4069-6c78-6c61-7bf6-c60968e45fbf
```

<span data-ttu-id="5db07-113">Isso altera o pool do Volume MeuVolume para um com a ID de 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span><span class="sxs-lookup"><span data-stu-id="5db07-113">This changes the pool for the volume MyVolume to one with the Id of 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span></span>

## <span data-ttu-id="5db07-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5db07-114">PARAMETERS</span></span>

### <span data-ttu-id="5db07-115">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="5db07-115">-AccountName</span></span>
<span data-ttu-id="5db07-116">O nome da conta da ANF</span><span class="sxs-lookup"><span data-stu-id="5db07-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="5db07-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5db07-117">-DefaultProfile</span></span>
<span data-ttu-id="5db07-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5db07-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5db07-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5db07-119">-InputObject</span></span>
<span data-ttu-id="5db07-120">O objeto de volume a ser movimentado</span><span class="sxs-lookup"><span data-stu-id="5db07-120">The volume object to move</span></span>

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

### <span data-ttu-id="5db07-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="5db07-121">-Name</span></span>
<span data-ttu-id="5db07-122">O nome do volume da ANF</span><span class="sxs-lookup"><span data-stu-id="5db07-122">The name of the ANF volume</span></span>

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

### <span data-ttu-id="5db07-123">-NewPoolResourceId</span><span class="sxs-lookup"><span data-stu-id="5db07-123">-NewPoolResourceId</span></span>
<span data-ttu-id="5db07-124">ResourceId do pool de capacidade para o que se mover.</span><span class="sxs-lookup"><span data-stu-id="5db07-124">ResourceId of the capacity pool to move to.</span></span>
<span data-ttu-id="5db07-125">UUID v4 usado para identificar o pool</span><span class="sxs-lookup"><span data-stu-id="5db07-125">UUID v4 used to identify the pool</span></span>

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

### <span data-ttu-id="5db07-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="5db07-126">-PoolName</span></span>
<span data-ttu-id="5db07-127">O nome do pool de ANF</span><span class="sxs-lookup"><span data-stu-id="5db07-127">The name of the ANF pool</span></span>

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

### <span data-ttu-id="5db07-128">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="5db07-128">-PoolObject</span></span>
<span data-ttu-id="5db07-129">O objeto de pool que contém o volume</span><span class="sxs-lookup"><span data-stu-id="5db07-129">The pool object containing the volume</span></span>

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

### <span data-ttu-id="5db07-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5db07-130">-ResourceGroupName</span></span>
<span data-ttu-id="5db07-131">O grupo de recursos do volume de ANF</span><span class="sxs-lookup"><span data-stu-id="5db07-131">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="5db07-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5db07-132">-ResourceId</span></span>
<span data-ttu-id="5db07-133">A ID do recurso do volume da ANF</span><span class="sxs-lookup"><span data-stu-id="5db07-133">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="5db07-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="5db07-134">-Confirm</span></span>
<span data-ttu-id="5db07-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5db07-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5db07-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5db07-136">-WhatIf</span></span>
<span data-ttu-id="5db07-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="5db07-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5db07-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5db07-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5db07-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5db07-139">CommonParameters</span></span>
<span data-ttu-id="5db07-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5db07-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5db07-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5db07-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5db07-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="5db07-142">INPUTS</span></span>

### <span data-ttu-id="5db07-143">System.String</span><span class="sxs-lookup"><span data-stu-id="5db07-143">System.String</span></span>

### <span data-ttu-id="5db07-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="5db07-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="5db07-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="5db07-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="5db07-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="5db07-146">OUTPUTS</span></span>

### <span data-ttu-id="5db07-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5db07-147">System.Boolean</span></span>

## <span data-ttu-id="5db07-148">Notas</span><span class="sxs-lookup"><span data-stu-id="5db07-148">NOTES</span></span>

## <span data-ttu-id="5db07-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5db07-149">RELATED LINKS</span></span>
