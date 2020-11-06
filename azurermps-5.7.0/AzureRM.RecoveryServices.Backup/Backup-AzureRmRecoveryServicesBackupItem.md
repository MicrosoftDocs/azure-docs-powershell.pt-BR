---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/backup-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Backup-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Backup-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: a7451855f62a9e0eab63936107d8431342badfb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439837"
---
# <span data-ttu-id="d29e9-101">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="d29e9-101">Backup-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="d29e9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d29e9-102">SYNOPSIS</span></span>
<span data-ttu-id="d29e9-103">Inicia um backup para um item de backup.</span><span class="sxs-lookup"><span data-stu-id="d29e9-103">Starts a backup for a Backup item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d29e9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d29e9-104">SYNTAX</span></span>

```
Backup-AzureRmRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d29e9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d29e9-105">DESCRIPTION</span></span>
<span data-ttu-id="d29e9-106">O cmdlet **backup-AzureRmRecoveryServicesBackupItem** inicia um backup para um item do Azure backup protegido que não está vinculado ao agendamento de backup.</span><span class="sxs-lookup"><span data-stu-id="d29e9-106">The **Backup-AzureRmRecoveryServicesBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="d29e9-107">Você pode fazer um backup inicial imediatamente após habilitar a proteção ou iniciar um backup após a falha de um backup agendado.</span><span class="sxs-lookup"><span data-stu-id="d29e9-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>

<span data-ttu-id="d29e9-108">Defina o contexto do cofre usando o cmdlet Set-AzureRmRecoveryServicesVaultContext antes de usar o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="d29e9-108">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="d29e9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d29e9-109">EXAMPLES</span></span>

### <span data-ttu-id="d29e9-110">Exemplo 1: iniciar um backup para um item de backup</span><span class="sxs-lookup"><span data-stu-id="d29e9-110">Example 1: Start a backup for a Backup item</span></span>
```
PS C:\> $NamedContainer = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "pstestv2vm1" 
PS C:\> $Item = Get-AzureRmRecoveryServicesBackupItem -Container $NamedContainer -WorkloadType AzureVM 
PS C:\> $Job = Backup-AzureRmRecoveryServicesItem -Item $Item
Operation        Status               StartTime            EndTime                   JOBID                           
------------     ---------            ------               ---------                 -------                                         
pstestv2vm1      Backup               InProgress           4/23/2016 5:00:30 PM      cf4b3ef5-2fac-4c8e-a215-d2eba4124f27
```

<span data-ttu-id="d29e9-111">O primeiro comando obtém o contêiner de backup do tipo AzureVM chamado pstestv2vm1 e, em seguida, armazena-o na variável $NamedContainer.</span><span class="sxs-lookup"><span data-stu-id="d29e9-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>

<span data-ttu-id="d29e9-112">O segundo comando obtém o item de backup correspondente ao contêiner no $NamedContainer e, em seguida, armazena-o na variável $Item.</span><span class="sxs-lookup"><span data-stu-id="d29e9-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>

<span data-ttu-id="d29e9-113">O último comando dispara o trabalho de backup para o item de backup em $Item.</span><span class="sxs-lookup"><span data-stu-id="d29e9-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

## <span data-ttu-id="d29e9-114">OS</span><span class="sxs-lookup"><span data-stu-id="d29e9-114">PARAMETERS</span></span>

### <span data-ttu-id="d29e9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d29e9-115">-DefaultProfile</span></span>
<span data-ttu-id="d29e9-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d29e9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d29e9-117">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="d29e9-117">-ExpiryDateTimeUTC</span></span>
<span data-ttu-id="d29e9-118">Especifica um tempo de expiração como um objeto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="d29e9-118">Specifies an expiry time as a **DateTime** object.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d29e9-119">-Item</span><span class="sxs-lookup"><span data-stu-id="d29e9-119">-Item</span></span>
<span data-ttu-id="d29e9-120">Especifica um item de backup para o qual esse cmdlet inicia uma operação de backup.</span><span class="sxs-lookup"><span data-stu-id="d29e9-120">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

```yaml
Type: ItemBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d29e9-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d29e9-121">-Confirm</span></span>
<span data-ttu-id="d29e9-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d29e9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d29e9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d29e9-123">-WhatIf</span></span>
<span data-ttu-id="d29e9-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d29e9-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d29e9-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d29e9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d29e9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d29e9-126">CommonParameters</span></span>
<span data-ttu-id="d29e9-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d29e9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d29e9-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d29e9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d29e9-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d29e9-129">INPUTS</span></span>

### <span data-ttu-id="d29e9-130">DateTime</span><span class="sxs-lookup"><span data-stu-id="d29e9-130">DateTime</span></span>
<span data-ttu-id="d29e9-131">O parâmetro ' ExpiryDateTimeUTC ' aceita o valor do tipo ' DateTime ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="d29e9-131">Parameter 'ExpiryDateTimeUTC' accepts value of type 'DateTime' from the pipeline</span></span>

### <span data-ttu-id="d29e9-132">Dobase</span><span class="sxs-lookup"><span data-stu-id="d29e9-132">ItemBase</span></span>
<span data-ttu-id="d29e9-133">O parâmetro ' item ' aceita o valor do tipo ' database ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="d29e9-133">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="d29e9-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d29e9-134">OUTPUTS</span></span>

### <span data-ttu-id="d29e9-135">Microsoft. Azure. Commands. Recoveryservices. backup. cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="d29e9-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="d29e9-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d29e9-136">NOTES</span></span>

## <span data-ttu-id="d29e9-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d29e9-137">RELATED LINKS</span></span>

[<span data-ttu-id="d29e9-138">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="d29e9-138">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="d29e9-139">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="d29e9-139">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="d29e9-140">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="d29e9-140">Restore-AzureRmRecoveryServicesBackupItem</span></span>](./Restore-AzureRmRecoveryServicesBackupItem.md)


