---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrinmageazurev2diskinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
ms.openlocfilehash: 115287c5892a83cd38e20080cdaee8ff531a612d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944698"
---
# <span data-ttu-id="df990-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="df990-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="df990-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="df990-102">SYNOPSIS</span></span>
<span data-ttu-id="df990-103">Cria um objeto de mapeamento de disco para discos de máquina virtual do vMWare a serem replicados.</span><span class="sxs-lookup"><span data-stu-id="df990-103">Creates a disk mapping object for vMWare virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="df990-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="df990-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId <String> -LogStorageAccountId <String>
 -DiskType <String> [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df990-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="df990-105">DESCRIPTION</span></span>
<span data-ttu-id="df990-106">Cria um objeto de mapeamento de disco que mapeia um disco de máquina virtual do vMWare para a conta de armazenamento do cache e destino o tipo de disco gerenciado (região de recuperação) a ser usado para replicar o disco.</span><span class="sxs-lookup"><span data-stu-id="df990-106">Creates a disk mapping object that maps an vMWare virtual machine disk to the cache storage account and target managed disk type (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="df990-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="df990-107">EXAMPLES</span></span>

### <span data-ttu-id="df990-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="df990-108">Example 1</span></span>
```powershell
PS C:> New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
```

<span data-ttu-id="df990-109">Crie um objeto de mapeamento de disco para discos de máquina virtual do vMWare a ser replicado. Usado durante a habilitação da proteção para o vMWare Machine.</span><span class="sxs-lookup"><span data-stu-id="df990-109">Create a disk mapping object for vMWare virtual machine disks to be replicated.Used during enable protection for vMWare machine.</span></span>

## <span data-ttu-id="df990-110">OS</span><span class="sxs-lookup"><span data-stu-id="df990-110">PARAMETERS</span></span>

### <span data-ttu-id="df990-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df990-111">-DefaultProfile</span></span>
<span data-ttu-id="df990-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="df990-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df990-113">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="df990-113">-DiskEncryptionSetId</span></span>
<span data-ttu-id="df990-114">Especifica a ID do recurso do conjunto de criptografia de disco a ser usado para a criptografia dos discos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="df990-114">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df990-115">-DiskId</span><span class="sxs-lookup"><span data-stu-id="df990-115">-DiskId</span></span>
<span data-ttu-id="df990-116">Especifique o DiskId do disco ao qual esse mapeamento corresponde.</span><span class="sxs-lookup"><span data-stu-id="df990-116">Specify the DiskId of the disk that this mapping corresponds to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df990-117">-Disktype</span><span class="sxs-lookup"><span data-stu-id="df990-117">-DiskType</span></span>
<span data-ttu-id="df990-118">Especifica o tipo de disco de recuperação.</span><span class="sxs-lookup"><span data-stu-id="df990-118">Specifies the Recovery disk type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df990-119">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="df990-119">-LogStorageAccountId</span></span>
<span data-ttu-id="df990-120">Especifica o log ou a ID da conta de armazenamento do cache a ser usada para armazenar logs de replicação.</span><span class="sxs-lookup"><span data-stu-id="df990-120">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df990-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="df990-121">-Confirm</span></span>
<span data-ttu-id="df990-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df990-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df990-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df990-123">-WhatIf</span></span>
<span data-ttu-id="df990-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="df990-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df990-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="df990-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df990-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df990-126">CommonParameters</span></span>
<span data-ttu-id="df990-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df990-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df990-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df990-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df990-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="df990-129">INPUTS</span></span>

### <span data-ttu-id="df990-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="df990-130">None</span></span>

## <span data-ttu-id="df990-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="df990-131">OUTPUTS</span></span>

### <span data-ttu-id="df990-132">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. AsrInMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="df990-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="df990-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="df990-133">NOTES</span></span>

## <span data-ttu-id="df990-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df990-134">RELATED LINKS</span></span>
