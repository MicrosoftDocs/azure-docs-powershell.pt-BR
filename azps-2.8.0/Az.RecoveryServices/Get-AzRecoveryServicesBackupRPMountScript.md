---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprpmountscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRPMountScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRPMountScript.md
ms.openlocfilehash: 6301c621de4399509c70271eb318983e91ebd121
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773004"
---
# <span data-ttu-id="52377-101">Get-AzRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="52377-101">Get-AzRecoveryServicesBackupRPMountScript</span></span>

## <span data-ttu-id="52377-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52377-102">SYNOPSIS</span></span>
<span data-ttu-id="52377-103">Baixa um script para montar todos os arquivos do ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="52377-103">Downloads a script to mount all the files of the recovery point.</span></span>

## <span data-ttu-id="52377-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52377-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupRPMountScript [-RecoveryPoint] <RecoveryPointBase> [[-Path] <String>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52377-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52377-105">DESCRIPTION</span></span>
<span data-ttu-id="52377-106">O cmdlet Get-AzRecoveryServicesBackupRPMountScript baixa um script que monta os volumes do ponto de recuperação no computador em que ele é executado.</span><span class="sxs-lookup"><span data-stu-id="52377-106">The Get-AzRecoveryServicesBackupRPMountScript cmdlet downloads a script which mounts the volumes of the recovery point on the machine where it is run.</span></span>

## <span data-ttu-id="52377-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52377-107">EXAMPLES</span></span>

### <span data-ttu-id="52377-108">Exemplo 1: montar um ponto de recuperação</span><span class="sxs-lookup"><span data-stu-id="52377-108">Example 1: Mount a recovery point</span></span>
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

<span data-ttu-id="52377-109">Quando o script for executado, ele montará os arquivos do ponto de recuperação $rp \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="52377-109">When the script is run, it will mount the files of the recovery point $rp\[0\]</span></span>

## <span data-ttu-id="52377-110">OS</span><span class="sxs-lookup"><span data-stu-id="52377-110">PARAMETERS</span></span>

### <span data-ttu-id="52377-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52377-111">-DefaultProfile</span></span>
<span data-ttu-id="52377-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52377-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52377-113">-Caminho</span><span class="sxs-lookup"><span data-stu-id="52377-113">-Path</span></span>
<span data-ttu-id="52377-114">Local onde o arquivo deve ser baixado em caso de recuperação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="52377-114">Location where the file should be downloaded in the case of file recovery.</span></span> <span data-ttu-id="52377-115">Se-path não for fornecido, o arquivo de script será baixado no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="52377-115">If -Path is not provided, the script file will be downloaded in the current directory.</span></span>

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

### <span data-ttu-id="52377-116">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="52377-116">-RecoveryPoint</span></span>
<span data-ttu-id="52377-117">Objeto de ponto de recuperação a ser restaurado</span><span class="sxs-lookup"><span data-stu-id="52377-117">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="52377-118">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="52377-118">-VaultId</span></span>
<span data-ttu-id="52377-119">ID do braço do cofre de serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="52377-119">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="52377-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="52377-120">-Confirm</span></span>
<span data-ttu-id="52377-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52377-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52377-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52377-122">-WhatIf</span></span>
<span data-ttu-id="52377-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="52377-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52377-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="52377-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52377-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52377-125">CommonParameters</span></span>
<span data-ttu-id="52377-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52377-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52377-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52377-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52377-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52377-128">INPUTS</span></span>

### <span data-ttu-id="52377-129">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="52377-129">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

### <span data-ttu-id="52377-130">System. String</span><span class="sxs-lookup"><span data-stu-id="52377-130">System.String</span></span>

## <span data-ttu-id="52377-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52377-131">OUTPUTS</span></span>

### <span data-ttu-id="52377-132">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. RPMountScriptDetails</span><span class="sxs-lookup"><span data-stu-id="52377-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RPMountScriptDetails</span></span>

## <span data-ttu-id="52377-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52377-133">NOTES</span></span>

## <span data-ttu-id="52377-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52377-134">RELATED LINKS</span></span>