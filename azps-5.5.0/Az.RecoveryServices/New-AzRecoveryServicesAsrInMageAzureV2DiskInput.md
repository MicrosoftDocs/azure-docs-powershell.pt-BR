---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrinmageazurev2diskinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
ms.openlocfilehash: 115287c5892a83cd38e20080cdaee8ff531a612d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114936"
---
# <span data-ttu-id="244a2-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="244a2-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="244a2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="244a2-102">SYNOPSIS</span></span>
<span data-ttu-id="244a2-103">Cria um objeto de mapeamento de disco para que discos de máquina virtuais vMWare sejam replicados.</span><span class="sxs-lookup"><span data-stu-id="244a2-103">Creates a disk mapping object for vMWare virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="244a2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="244a2-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId <String> -LogStorageAccountId <String>
 -DiskType <String> [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="244a2-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="244a2-105">DESCRIPTION</span></span>
<span data-ttu-id="244a2-106">Cria um objeto de mapeamento de disco que mapeia um disco de máquina virtual vMWare para a conta de armazenamento em cache e o tipo de disco gerenciado de destino (região de recuperação) a ser usado para replicar o disco.</span><span class="sxs-lookup"><span data-stu-id="244a2-106">Creates a disk mapping object that maps an vMWare virtual machine disk to the cache storage account and target managed disk type (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="244a2-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="244a2-107">EXAMPLES</span></span>

### <span data-ttu-id="244a2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="244a2-108">Example 1</span></span>
```powershell
PS C:> New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
```

<span data-ttu-id="244a2-109">Crie um objeto de mapeamento de disco para que discos de máquina virtuais vMWare sejam replicados. Usado durante a proteção de habilitar para o computador vMWare.</span><span class="sxs-lookup"><span data-stu-id="244a2-109">Create a disk mapping object for vMWare virtual machine disks to be replicated.Used during enable protection for vMWare machine.</span></span>

## <span data-ttu-id="244a2-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="244a2-110">PARAMETERS</span></span>

### <span data-ttu-id="244a2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="244a2-111">-DefaultProfile</span></span>
<span data-ttu-id="244a2-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="244a2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="244a2-113">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="244a2-113">-DiskEncryptionSetId</span></span>
<span data-ttu-id="244a2-114">Especifica a ID do recurso do conjunto de criptografia de disco, a ser usado para a criptografia dos discos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="244a2-114">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

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

### <span data-ttu-id="244a2-115">-DiskId</span><span class="sxs-lookup"><span data-stu-id="244a2-115">-DiskId</span></span>
<span data-ttu-id="244a2-116">Especifique a DiskId do disco ao qual esse mapeamento corresponde.</span><span class="sxs-lookup"><span data-stu-id="244a2-116">Specify the DiskId of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="244a2-117">-DiskType</span><span class="sxs-lookup"><span data-stu-id="244a2-117">-DiskType</span></span>
<span data-ttu-id="244a2-118">Especifica o tipo de disco Recuperação.</span><span class="sxs-lookup"><span data-stu-id="244a2-118">Specifies the Recovery disk type.</span></span>

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

### <span data-ttu-id="244a2-119">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="244a2-119">-LogStorageAccountId</span></span>
<span data-ttu-id="244a2-120">Especifica a ID da conta de armazenamento em cache ou log a ser usada para armazenar logs de replicação.</span><span class="sxs-lookup"><span data-stu-id="244a2-120">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="244a2-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="244a2-121">-Confirm</span></span>
<span data-ttu-id="244a2-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="244a2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="244a2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="244a2-123">-WhatIf</span></span>
<span data-ttu-id="244a2-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="244a2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="244a2-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="244a2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="244a2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="244a2-126">CommonParameters</span></span>
<span data-ttu-id="244a2-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="244a2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="244a2-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="244a2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="244a2-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="244a2-129">INPUTS</span></span>

### <span data-ttu-id="244a2-130">Nenhum</span><span class="sxs-lookup"><span data-stu-id="244a2-130">None</span></span>

## <span data-ttu-id="244a2-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="244a2-131">OUTPUTS</span></span>

### <span data-ttu-id="244a2-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="244a2-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="244a2-133">Notas</span><span class="sxs-lookup"><span data-stu-id="244a2-133">NOTES</span></span>

## <span data-ttu-id="244a2-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="244a2-134">RELATED LINKS</span></span>
