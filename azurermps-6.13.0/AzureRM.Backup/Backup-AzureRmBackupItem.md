---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9FF4F649-F50C-4C27-842F-1CD6C5BC7A2B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/backup-azurermbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Backup-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Backup-AzureRmBackupItem.md
ms.openlocfilehash: e87ab3ec04378dc97e144d2b444ee5398ff4f4f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433324"
---
# <span data-ttu-id="d17a3-101">Backup-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="d17a3-101">Backup-AzureRmBackupItem</span></span>

## <span data-ttu-id="d17a3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d17a3-102">SYNOPSIS</span></span>
<span data-ttu-id="d17a3-103">Inicia um backup para um item de backup.</span><span class="sxs-lookup"><span data-stu-id="d17a3-103">Starts a backup for a Backup item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d17a3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d17a3-104">SYNTAX</span></span>

```
Backup-AzureRmBackupItem [-Item] <AzureRMBackupItem> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d17a3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d17a3-105">DESCRIPTION</span></span>
<span data-ttu-id="d17a3-106">O cmdlet **backup-AzureRmBackupItem** inicia um backup para um item do Azure backup protegido que não está vinculado ao agendamento de backup.</span><span class="sxs-lookup"><span data-stu-id="d17a3-106">The **Backup-AzureRmBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="d17a3-107">Você pode fazer um backup inicial imediatamente após habilitar a proteção ou iniciar um backup após a falha de um backup agendado.</span><span class="sxs-lookup"><span data-stu-id="d17a3-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>
<span data-ttu-id="d17a3-108">Se um trabalho de backup existente estiver em execução, esse cmdlet falhará.</span><span class="sxs-lookup"><span data-stu-id="d17a3-108">If an existing backup job is running, this cmdlet fails.</span></span>

## <span data-ttu-id="d17a3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d17a3-109">EXAMPLES</span></span>

### <span data-ttu-id="d17a3-110">Exemplo 1: iniciar o backup de uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="d17a3-110">Example 1: Start to back up a virtual machine</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> Get-AzureRmBackupItem -Container $Container | Backup-AzureRmBackupItem
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
```

<span data-ttu-id="d17a3-111">O primeiro comando obtém o cofre chamado Vault03 usando o cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="d17a3-111">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="d17a3-112">O comando armazena esse objeto na variável $Vault.</span><span class="sxs-lookup"><span data-stu-id="d17a3-112">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="d17a3-113">O segundo comando obtém um contêiner que tem o nome especificado no cofre no $Vault usando o cmdlet Get-AzureRmBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="d17a3-113">The second command gets a container that has the specified name in the vault in $Vault by using the Get-AzureRmBackupContainer cmdlet.</span></span>
<span data-ttu-id="d17a3-114">O comando armazena esse objeto na variável $Container.</span><span class="sxs-lookup"><span data-stu-id="d17a3-114">The command stores that object in the $Container variable.</span></span>
<span data-ttu-id="d17a3-115">O último comando obtém os itens de backup no $Container usando o cmdlet Get-AzureRmBackupItem.</span><span class="sxs-lookup"><span data-stu-id="d17a3-115">The last command gets the backup items in $Container by using the Get-AzureRmBackupItem cmdlet.</span></span>
<span data-ttu-id="d17a3-116">O comando passa os itens para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="d17a3-116">The command passes the items to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d17a3-117">O cmdlet atual começa a fazer backup da máquina virtual no contêiner.</span><span class="sxs-lookup"><span data-stu-id="d17a3-117">The current cmdlet starts backing up the virtual machine in the container.</span></span>

## <span data-ttu-id="d17a3-118">OS</span><span class="sxs-lookup"><span data-stu-id="d17a3-118">PARAMETERS</span></span>

### <span data-ttu-id="d17a3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d17a3-119">-DefaultProfile</span></span>
<span data-ttu-id="d17a3-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d17a3-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d17a3-121">-Item</span><span class="sxs-lookup"><span data-stu-id="d17a3-121">-Item</span></span>
<span data-ttu-id="d17a3-122">Especifica um item de backup para o qual esse cmdlet inicia uma operação de backup.</span><span class="sxs-lookup"><span data-stu-id="d17a3-122">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d17a3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d17a3-123">CommonParameters</span></span>
<span data-ttu-id="d17a3-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d17a3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d17a3-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d17a3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d17a3-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d17a3-126">INPUTS</span></span>

### <span data-ttu-id="d17a3-127">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupItem</span><span class="sxs-lookup"><span data-stu-id="d17a3-127">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem</span></span>
<span data-ttu-id="d17a3-128">Parâmetros: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d17a3-128">Parameters: Item (ByValue)</span></span>

## <span data-ttu-id="d17a3-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d17a3-129">OUTPUTS</span></span>

### <span data-ttu-id="d17a3-130">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="d17a3-130">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="d17a3-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d17a3-131">NOTES</span></span>

## <span data-ttu-id="d17a3-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d17a3-132">RELATED LINKS</span></span>

[<span data-ttu-id="d17a3-133">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="d17a3-133">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="d17a3-134">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="d17a3-134">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="d17a3-135">Restore-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="d17a3-135">Restore-AzureRmBackupItem</span></span>](./Restore-AzureRmBackupItem.md)


