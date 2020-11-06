---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackuprpmountscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRPMountScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRPMountScript.md
ms.openlocfilehash: 0f3f0292b4f348207bf80d5e04c63dc45be69fa3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427496"
---
# <span data-ttu-id="aded8-101">Get-AzureRmRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="aded8-101">Get-AzureRmRecoveryServicesBackupRPMountScript</span></span>

## <span data-ttu-id="aded8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aded8-102">SYNOPSIS</span></span>
<span data-ttu-id="aded8-103">Baixa um script para montar todos os arquivos do ponto de recuperação.</span><span class="sxs-lookup"><span data-stu-id="aded8-103">Downloads a script to mount all the files of the recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aded8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aded8-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupRPMountScript [-RecoveryPoint] <RecoveryPointBase> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aded8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aded8-105">DESCRIPTION</span></span>
<span data-ttu-id="aded8-106">O cmdlet Get-AzureRmRecoveryServicesBackupRPMountScript baixa um script que monta os volumes do ponto de recuperação no computador em que ele é executado.</span><span class="sxs-lookup"><span data-stu-id="aded8-106">The Get-AzureRmRecoveryServicesBackupRPMountScript cmdlet downloads a script which mounts the volumes of the recovery point on the machine where it is run.</span></span>

## <span data-ttu-id="aded8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aded8-107">EXAMPLES</span></span>

### <span data-ttu-id="aded8-108">Exemplo 1: montar um ponto de recuperação</span><span class="sxs-lookup"><span data-stu-id="aded8-108">Example 1: Mount a recovery point</span></span>
```
PS C:\> $namedContainer = Get-AzureRmRecoveryServicesBackupContainer  -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM"
PS C:\> $backupitem = Get-AzureRmRecoveryServicesBackupItem -Container $namedContainer  -WorkloadType "AzureVM"
PS C:\> $startDate = (Get-Date).AddDays(-7)
PS C:\> $endDate = Get-Date
PS C:\> $rp = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $backupitem -StartDate $startdate.ToUniversalTime() -EndDate $enddate.ToUniversalTime()

To mount files of the latest recovery point, obtain the script by

PS C:\> Get-AzureRmRecoveryServicesBackupRPMountScript -RecoveryPoint $rp[0]

OsType  Password        Filename
------  --------        --------
Windows e3632984e51f496 V2VM_wus2_8287309959960546283_451516692429_cbd6061f7fc543c489f1974d33659fed07a6e0c2e08740.exe
```

<span data-ttu-id="aded8-109">Quando o script for executado, ele montará os arquivos do ponto de recuperação $rp \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="aded8-109">When the script is run, it will mount the files of the recovery point $rp\[0\]</span></span>

## <span data-ttu-id="aded8-110">OS</span><span class="sxs-lookup"><span data-stu-id="aded8-110">PARAMETERS</span></span>

### <span data-ttu-id="aded8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aded8-111">-DefaultProfile</span></span>
<span data-ttu-id="aded8-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aded8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aded8-113">-Caminho</span><span class="sxs-lookup"><span data-stu-id="aded8-113">-Path</span></span>
<span data-ttu-id="aded8-114">Local onde o arquivo deve ser baixado em caso de recuperação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="aded8-114">Location where the file should be downloaded in the case of file recovery.</span></span> <span data-ttu-id="aded8-115">Se-path não for fornecido, o arquivo de script será baixado no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="aded8-115">If -Path is not provided, the script file will be downloaded in the current directory.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aded8-116">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="aded8-116">-RecoveryPoint</span></span>
<span data-ttu-id="aded8-117">Objeto de ponto de recuperação a ser restaurado</span><span class="sxs-lookup"><span data-stu-id="aded8-117">Recovery point object to be restored</span></span>

```yaml
Type: RecoveryPointBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aded8-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="aded8-118">-Confirm</span></span>
<span data-ttu-id="aded8-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aded8-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aded8-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aded8-120">-WhatIf</span></span>
<span data-ttu-id="aded8-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="aded8-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aded8-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aded8-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aded8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aded8-123">CommonParameters</span></span>
<span data-ttu-id="aded8-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aded8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aded8-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aded8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aded8-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aded8-126">INPUTS</span></span>

### <span data-ttu-id="aded8-127">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="aded8-127">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="aded8-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aded8-128">OUTPUTS</span></span>

### <span data-ttu-id="aded8-129">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. RPMountScriptDetails</span><span class="sxs-lookup"><span data-stu-id="aded8-129">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RPMountScriptDetails</span></span>

## <span data-ttu-id="aded8-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aded8-130">NOTES</span></span>

## <span data-ttu-id="aded8-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aded8-131">RELATED LINKS</span></span>

