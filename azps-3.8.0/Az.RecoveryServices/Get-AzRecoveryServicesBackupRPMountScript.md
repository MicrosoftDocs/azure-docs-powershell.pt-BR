---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprpmountscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRPMountScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRPMountScript.md
ms.openlocfilehash: 427da45eed5e2e9e27421e67d9e6e776d9106367
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944731"
---
# <span data-ttu-id="b8d1a-101">Get-AzRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="b8d1a-101">Get-AzRecoveryServicesBackupRPMountScript</span></span>

## <span data-ttu-id="b8d1a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b8d1a-102">SYNOPSIS</span></span>
<span data-ttu-id="b8d1a-103">Baixa um script para montar todos os arquivos do ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="b8d1a-103">Downloads a script to mount all the files of the recovery point.</span></span>

## <span data-ttu-id="b8d1a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8d1a-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupRPMountScript [-RecoveryPoint] <RecoveryPointBase> [[-Path] <String>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8d1a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b8d1a-105">DESCRIPTION</span></span>
<span data-ttu-id="b8d1a-106">O cmdlet Get-AzRecoveryServicesBackupRPMountScript baixa um script que monta os volumes do ponto de recuperação no computador em que ele é executado.</span><span class="sxs-lookup"><span data-stu-id="b8d1a-106">The Get-AzRecoveryServicesBackupRPMountScript cmdlet downloads a script which mounts the volumes of the recovery point on the machine where it is run.</span></span>

## <span data-ttu-id="b8d1a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b8d1a-107">EXAMPLES</span></span>

### <span data-ttu-id="b8d1a-108">Exemplo 1: montar um ponto de recuperação</span><span class="sxs-lookup"><span data-stu-id="b8d1a-108">Example 1: Mount a recovery point</span></span>
```
PS C:\> $namedContainer = Get-AzRecoveryServicesBackupContainer  -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM"
PS C:\> $backupitem = Get-AzRecoveryServicesBackupItem -Container $namedContainer  -WorkloadType "AzureVM"
PS C:\> $startDate = (Get-Date).AddDays(-7)
PS C:\> $endDate = Get-Date
PS C:\> $rp = Get-AzRecoveryServicesBackupRecoveryPoint -Item $backupitem -StartDate $startdate.ToUniversalTime() -EndDate $enddate.ToUniversalTime()

To mount files of the latest recovery point, obtain the script by

PS C:\> Get-AzRecoveryServicesBackupRPMountScript -RecoveryPoint $rp[0]

OsType  Password        Filename
------  --------        --------
Windows e3632984e51f496 V2VM_wus2_8287309959960546283_451516692429_cbd6061f7fc543c489f1974d33659fed07a6e0c2e08740.exe
```

<span data-ttu-id="b8d1a-109">Quando o script for executado, ele montará os arquivos do ponto de recuperação $rp \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="b8d1a-109">When the script is run, it will mount the files of the recovery point $rp\[0\]</span></span>

## <span data-ttu-id="b8d1a-110">OS</span><span class="sxs-lookup"><span data-stu-id="b8d1a-110">PARAMETERS</span></span>

### <span data-ttu-id="b8d1a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8d1a-111">-DefaultProfile</span></span>
<span data-ttu-id="b8d1a-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b8d1a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8d1a-113">-Caminho</span><span class="sxs-lookup"><span data-stu-id="b8d1a-113">-Path</span></span>
<span data-ttu-id="b8d1a-114">Local onde o arquivo deve ser baixado em caso de recuperação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="b8d1a-114">Location where the file should be downloaded in the case of file recovery.</span></span> <span data-ttu-id="b8d1a-115">Se-path não for fornecido, o arquivo de script será baixado no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="b8d1a-115">If -Path is not provided, the script file will be downloaded in the current directory.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d1a-116">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="b8d1a-116">-RecoveryPoint</span></span>
<span data-ttu-id="b8d1a-117">Objeto de ponto de recuperação a ser restaurado</span><span class="sxs-lookup"><span data-stu-id="b8d1a-117">Recovery point object to be restored</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8d1a-118">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="b8d1a-118">-VaultId</span></span>
<span data-ttu-id="b8d1a-119">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="b8d1a-119">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8d1a-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b8d1a-120">-Confirm</span></span>
<span data-ttu-id="b8d1a-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8d1a-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d1a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8d1a-122">-WhatIf</span></span>
<span data-ttu-id="b8d1a-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b8d1a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8d1a-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b8d1a-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d1a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8d1a-125">CommonParameters</span></span>
<span data-ttu-id="b8d1a-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8d1a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8d1a-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8d1a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8d1a-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b8d1a-128">INPUTS</span></span>

### <span data-ttu-id="b8d1a-129">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="b8d1a-129">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

### <span data-ttu-id="b8d1a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b8d1a-130">System.String</span></span>

## <span data-ttu-id="b8d1a-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b8d1a-131">OUTPUTS</span></span>

### <span data-ttu-id="b8d1a-132">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. RPMountScriptDetails</span><span class="sxs-lookup"><span data-stu-id="b8d1a-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RPMountScriptDetails</span></span>

## <span data-ttu-id="b8d1a-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b8d1a-133">NOTES</span></span>

## <span data-ttu-id="b8d1a-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8d1a-134">RELATED LINKS</span></span>
