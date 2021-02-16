---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditemDisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: a5ac137692c8945ba58e848ccca530bd4bc99ed2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113369"
---
# <span data-ttu-id="34f98-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="34f98-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="34f98-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="34f98-102">SYNOPSIS</span></span>
<span data-ttu-id="34f98-103">Remove discos para replicação de item protegido.</span><span class="sxs-lookup"><span data-stu-id="34f98-103">Removes disks to replication protected item.</span></span>

## <span data-ttu-id="34f98-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="34f98-104">SYNTAX</span></span>

### <span data-ttu-id="34f98-105">AzureToAzure (Padrão)</span><span class="sxs-lookup"><span data-stu-id="34f98-105">AzureToAzure (Default)</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -VhdUri <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="34f98-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="34f98-106">AzureToAzureManagedDisk</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -DiskId <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="34f98-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="34f98-107">DESCRIPTION</span></span>
<span data-ttu-id="34f98-108">O cmdlet **Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk** remove o disco do item protegido por replicação asR.</span><span class="sxs-lookup"><span data-stu-id="34f98-108">The **Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet removes the disk from the ASR replication protected item.</span></span>

## <span data-ttu-id="34f98-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="34f98-109">EXAMPLES</span></span>

### <span data-ttu-id="34f98-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="34f98-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -VhdUri $vhdUri
```

<span data-ttu-id="34f98-111">Inicie a operação para remover o disco especificado do VM de proteção para disco nãomanado.</span><span class="sxs-lookup"><span data-stu-id="34f98-111">Start the operation to remove specified disk from protection VM for unManaged disk.</span></span>

### <span data-ttu-id="34f98-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="34f98-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
```

<span data-ttu-id="34f98-113">Inicie a operação para remover o disco especificado da VM de proteção para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="34f98-113">Start the operation to remove specified disk from protection VM for Managed disk.</span></span>

### <span data-ttu-id="34f98-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="34f98-114">Example 3</span></span>
```
PS C:\>  $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
PS C:\>  Get-AzRecoveryServicesAsrJob -name $currentJob.id
```

<span data-ttu-id="34f98-115">Inicia a operação para remover o disco especificado e retorna o trabalho ASR usado para controlar a operação de remover disco protegido.</span><span class="sxs-lookup"><span data-stu-id="34f98-115">Starts the operation to remove the specified disk and returns the ASR job used to track the remove protected disk operation.</span></span>

## <span data-ttu-id="34f98-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="34f98-116">PARAMETERS</span></span>

### <span data-ttu-id="34f98-117">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="34f98-117">-Confirm</span></span>
<span data-ttu-id="34f98-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34f98-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34f98-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34f98-119">-DefaultProfile</span></span>
<span data-ttu-id="34f98-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="34f98-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34f98-121">-DiskId</span><span class="sxs-lookup"><span data-stu-id="34f98-121">-DiskId</span></span>
<span data-ttu-id="34f98-122">Especifica a lista de IDs de disco gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="34f98-122">Specifies the list of managed disk Ids.</span></span>

```yaml
Type: String[]
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34f98-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34f98-123">-InputObject</span></span>
<span data-ttu-id="34f98-124">O objeto de entrada para o cmdlet: o objeto de item protegido de replicação ASR correspondente ao disco a ser removido.</span><span class="sxs-lookup"><span data-stu-id="34f98-124">The input object to the cmdlet: The ASR replication protected item object corresponding to which disk is to be removed.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34f98-125">-HighdUri</span><span class="sxs-lookup"><span data-stu-id="34f98-125">-VhdUri</span></span>
<span data-ttu-id="34f98-126">Especifica a lista de Uri's.</span><span class="sxs-lookup"><span data-stu-id="34f98-126">Specifies the list of vhd Uri's.</span></span>

```yaml
Type: String[]
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34f98-127">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="34f98-127">-WaitForCompletion</span></span>
<span data-ttu-id="34f98-128">Aguarde a conclusão</span><span class="sxs-lookup"><span data-stu-id="34f98-128">Wait For Completion</span></span>

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

### <span data-ttu-id="34f98-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34f98-129">-WhatIf</span></span>
<span data-ttu-id="34f98-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="34f98-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34f98-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="34f98-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34f98-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34f98-132">CommonParameters</span></span>
<span data-ttu-id="34f98-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34f98-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34f98-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="34f98-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34f98-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="34f98-135">INPUTS</span></span>

### <span data-ttu-id="34f98-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="34f98-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="34f98-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="34f98-137">OUTPUTS</span></span>

### <span data-ttu-id="34f98-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="34f98-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="34f98-139">Notas</span><span class="sxs-lookup"><span data-stu-id="34f98-139">NOTES</span></span>

## <span data-ttu-id="34f98-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="34f98-140">RELATED LINKS</span></span>
