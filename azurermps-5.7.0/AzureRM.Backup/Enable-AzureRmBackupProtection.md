---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: DD150A2C-27D5-4119-9B43-FAB82F9F7D5B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/enable-azurermbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupProtection.md
ms.openlocfilehash: 87f269042b6d0f660f621a865dda7619afd9be5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609532"
---
# <span data-ttu-id="38902-101">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="38902-101">Enable-AzureRmBackupProtection</span></span>

## <span data-ttu-id="38902-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="38902-102">SYNOPSIS</span></span>
<span data-ttu-id="38902-103">Associa um item a uma política de proteção de backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="38902-103">Associates an item with an Azure Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38902-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38902-104">SYNTAX</span></span>

```
Enable-AzureRmBackupProtection -Policy <AzureRMBackupProtectionPolicy>
 [-Item] <AzureRMBackupContainerContextObject> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38902-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="38902-105">DESCRIPTION</span></span>
<span data-ttu-id="38902-106">O cmdlet **Enable-AzureRmBackupProtection** associa um item a uma política de proteção de backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="38902-106">The **Enable-AzureRmBackupProtection** cmdlet associates an item with an Azure Backup protection policy.</span></span>
<span data-ttu-id="38902-107">Para habilitar uma política de proteção, você deve primeiro ter um item de backup existente e uma política existente.</span><span class="sxs-lookup"><span data-stu-id="38902-107">To enable a protection policy, you must first have an existing backup item and an existing policy.</span></span>
<span data-ttu-id="38902-108">Ambas devem pertencer ao mesmo cofre de backup.</span><span class="sxs-lookup"><span data-stu-id="38902-108">Both must belong to the same Backup vault.</span></span>
<span data-ttu-id="38902-109">O agendamento de backup faz a cópia inicial completa para o item e a cópia incremental dos backups subsequentes.</span><span class="sxs-lookup"><span data-stu-id="38902-109">The backup schedule does the full initial copy for the item and the incremental copy for the subsequent backups.</span></span>

## <span data-ttu-id="38902-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="38902-110">EXAMPLES</span></span>

### <span data-ttu-id="38902-111">Exemplo 1: habilitar a proteção em uma máquina virtual do Azure</span><span class="sxs-lookup"><span data-stu-id="38902-111">Example 1: Enable protection on an Azure virtual machine</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Policy = Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DefaultPolicy"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered | Get-AzureRmBackupItem | Enable-AzureRmBackupProtection -Policy $Policy
WorkloadName    Operation        Status          StartTime              EndTime
------------    ---------        ------          ---------              -------
co03-vm         ConfigureBackup  Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
```

<span data-ttu-id="38902-112">O primeiro comando obtém o cofre chamado Vault03 usando o cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="38902-112">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="38902-113">O comando armazena esse objeto na variável $Vault.</span><span class="sxs-lookup"><span data-stu-id="38902-113">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="38902-114">O segundo comando obtém a política de proteção de backup chamada DefaultPolicy para o cofre em $Vault.</span><span class="sxs-lookup"><span data-stu-id="38902-114">The second command gets the Backup protection policy named DefaultPolicy for the vault in $Vault.</span></span>
<span data-ttu-id="38902-115">O comando armazena esse objeto na variável $Policy.</span><span class="sxs-lookup"><span data-stu-id="38902-115">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="38902-116">O comando final usa o operador pipeline para passar valores de um cmdlet para o seguinte.</span><span class="sxs-lookup"><span data-stu-id="38902-116">The final command uses the pipeline operator to pass values from one cmdlet to the next.</span></span>
<span data-ttu-id="38902-117">Ele obtém um contêiner, usando o cmdlet Get-AzureRmBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="38902-117">It gets a container, by using the Get-AzureRmBackupContainer cmdlet.</span></span>
<span data-ttu-id="38902-118">O comando obtém o item de backup desse contêiner usando o cmdlet Get-AzureRmBackupItem.</span><span class="sxs-lookup"><span data-stu-id="38902-118">The command gets the backup item from that container by using the Get-AzureRmBackupItem cmdlet.</span></span>
<span data-ttu-id="38902-119">O cmdlet atual habilita a política armazenada em $Policy para o item que o comando passa para esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38902-119">The current cmdlet enables the policy stored in $Policy for the item that the command passes to that cmdlet.</span></span>

## <span data-ttu-id="38902-120">OS</span><span class="sxs-lookup"><span data-stu-id="38902-120">PARAMETERS</span></span>

### <span data-ttu-id="38902-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38902-121">-DefaultProfile</span></span>
<span data-ttu-id="38902-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="38902-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38902-123">-Item</span><span class="sxs-lookup"><span data-stu-id="38902-123">-Item</span></span>
<span data-ttu-id="38902-124">Especifica o item de backup para o qual esse cmdlet habilita a proteção.</span><span class="sxs-lookup"><span data-stu-id="38902-124">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="38902-125">Para obter um **AzureRmBackupItem** , use o cmdlet Get-AzureRmBackupItem.</span><span class="sxs-lookup"><span data-stu-id="38902-125">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

```yaml
Type: AzureRMBackupContainerContextObject
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38902-126">-Política</span><span class="sxs-lookup"><span data-stu-id="38902-126">-Policy</span></span>
<span data-ttu-id="38902-127">Especifica a política de proteção que este cmdlet associa a um item.</span><span class="sxs-lookup"><span data-stu-id="38902-127">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="38902-128">Para obter um objeto **AzureRmBackupProtectionPolicy** , use o cmdlet Get-AzureRmBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="38902-128">To obtain an **AzureRmBackupProtectionPolicy** object, use the Get-AzureRmBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38902-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38902-129">CommonParameters</span></span>
<span data-ttu-id="38902-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38902-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38902-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38902-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38902-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="38902-132">INPUTS</span></span>

### <span data-ttu-id="38902-133">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="38902-133">AzureRmBackupItem</span></span>

## <span data-ttu-id="38902-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="38902-134">OUTPUTS</span></span>

### <span data-ttu-id="38902-135">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="38902-135">AzureRmBackupJob</span></span>

## <span data-ttu-id="38902-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="38902-136">NOTES</span></span>

## <span data-ttu-id="38902-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38902-137">RELATED LINKS</span></span>

[<span data-ttu-id="38902-138">Backup-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="38902-138">Backup-AzureRmBackupItem</span></span>](./Backup-AzureRmBackupItem.md)

[<span data-ttu-id="38902-139">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="38902-139">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="38902-140">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="38902-140">Get-AzureRmBackupProtectionPolicy</span></span>](./Get-AzureRmBackupProtectionPolicy.md)


