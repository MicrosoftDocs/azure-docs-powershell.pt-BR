---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6778E018-B6CC-468A-823E-3DA047EA6B52
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupRecoveryPoint.md
ms.openlocfilehash: 2805ebfd5849306dadb4cf913660c8fac1602d79
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431081"
---
# <span data-ttu-id="081f3-101">Get-AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="081f3-101">Get-AzureRmBackupRecoveryPoint</span></span>

## <span data-ttu-id="081f3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="081f3-102">SYNOPSIS</span></span>
<span data-ttu-id="081f3-103">Obtém os pontos de recuperação para um item de backup.</span><span class="sxs-lookup"><span data-stu-id="081f3-103">Gets the recovery points for a backed up item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="081f3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="081f3-104">SYNTAX</span></span>

```
Get-AzureRmBackupRecoveryPoint [[-RecoveryPointId] <String>] [-Item] <AzureRMBackupItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="081f3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="081f3-105">DESCRIPTION</span></span>
<span data-ttu-id="081f3-106">O cmdlet **Get-AzureRmBackupRecoveryPoint** Obtém os pontos de recuperação para um item do Azure backup em backup.</span><span class="sxs-lookup"><span data-stu-id="081f3-106">The **Get-AzureRmBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="081f3-107">Após o backup de um item, o backup armazena um ou mais pontos de recuperação.</span><span class="sxs-lookup"><span data-stu-id="081f3-107">After an item has been backed up, Backup stores one or more recovery points.</span></span>

## <span data-ttu-id="081f3-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="081f3-108">EXAMPLES</span></span>

### <span data-ttu-id="081f3-109">Exemplo 1: obter pontos de recuperação para um item</span><span class="sxs-lookup"><span data-stu-id="081f3-109">Example 1: Get recovery points for an item</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> $BackupItem = Get-AzureRmBackupItem -Container $Container
PS C:\> Get-AzureRmBackupRecoveryPoint -Item $BackupItem
RecoveryPointId    RecoveryPointType  RecoveryPointTime      ContainerName
---------------    -----------------  -----------------      -------------
15273496567119     AppConsistent      26-Aug-15 12:27:38 PM  iaasvmcontainer;conto02-vm;conto0...
```

<span data-ttu-id="081f3-110">O primeiro comando obtém o cofre chamado Vault03 usando o cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="081f3-110">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="081f3-111">O comando armazena esse objeto na variável $Vault.</span><span class="sxs-lookup"><span data-stu-id="081f3-111">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="081f3-112">O segundo comando obtém um contêiner que tem o nome especificado no cofre no $Vault usando o cmdlet **Get-AzureRmBackupContainer** .</span><span class="sxs-lookup"><span data-stu-id="081f3-112">The second command gets a container that has the specified name in the vault in $Vault by using the **Get-AzureRmBackupContainer** cmdlet.</span></span>
<span data-ttu-id="081f3-113">O comando armazena esse objeto na variável $Container.</span><span class="sxs-lookup"><span data-stu-id="081f3-113">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="081f3-114">O terceiro comando obtém o item de backup no contêiner no $Container usando o cmdlet **Get-AzureRmBackupItem** .</span><span class="sxs-lookup"><span data-stu-id="081f3-114">The third command gets the backup item in the container in $Container by using the **Get-AzureRmBackupItem** cmdlet.</span></span>
<span data-ttu-id="081f3-115">O comando armazena esse objeto na variável $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="081f3-115">The command stores that object in the $BackupItem variable.</span></span>

<span data-ttu-id="081f3-116">O comando final Obtém pontos de recuperação para o item em $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="081f3-116">The final command gets recovery points for the item in $BackupItem.</span></span>

## <span data-ttu-id="081f3-117">OS</span><span class="sxs-lookup"><span data-stu-id="081f3-117">PARAMETERS</span></span>

### <span data-ttu-id="081f3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="081f3-118">-DefaultProfile</span></span>
<span data-ttu-id="081f3-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="081f3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="081f3-120">-Item</span><span class="sxs-lookup"><span data-stu-id="081f3-120">-Item</span></span>
<span data-ttu-id="081f3-121">Especifica o item para o qual esse cmdlet recebe pontos de recuperação.</span><span class="sxs-lookup"><span data-stu-id="081f3-121">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="081f3-122">Para obter um **AzureRmBackupItem** , use o cmdlet Get-AzureRmBackupItem.</span><span class="sxs-lookup"><span data-stu-id="081f3-122">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

```yaml
Type: AzureRMBackupItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="081f3-123">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="081f3-123">-RecoveryPointId</span></span>
<span data-ttu-id="081f3-124">Especifica a ID de um ponto de recuperação que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="081f3-124">Specifies the ID of a recovery point that this cmdlet gets.</span></span>

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

### <span data-ttu-id="081f3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="081f3-125">CommonParameters</span></span>
<span data-ttu-id="081f3-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="081f3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="081f3-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="081f3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="081f3-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="081f3-128">INPUTS</span></span>

### <span data-ttu-id="081f3-129">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="081f3-129">AzureRmBackupItem</span></span>

## <span data-ttu-id="081f3-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="081f3-130">OUTPUTS</span></span>

### <span data-ttu-id="081f3-131">AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="081f3-131">AzureRmBackupRecoveryPoint</span></span>

## <span data-ttu-id="081f3-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="081f3-132">NOTES</span></span>

## <span data-ttu-id="081f3-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="081f3-133">RELATED LINKS</span></span>

[<span data-ttu-id="081f3-134">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="081f3-134">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="081f3-135">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="081f3-135">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="081f3-136">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="081f3-136">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


