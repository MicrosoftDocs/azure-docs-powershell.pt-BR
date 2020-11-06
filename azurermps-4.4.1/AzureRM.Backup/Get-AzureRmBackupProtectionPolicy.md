---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: B3B708C5-776E-4F1C-BA0B-492CD9057794
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: 08cfb4279199455b14794a890b398fd954cb4cd3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428288"
---
# <span data-ttu-id="9d9a4-101">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9d9a4-101">Get-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="9d9a4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9d9a4-102">SYNOPSIS</span></span>
<span data-ttu-id="9d9a4-103">Obtém políticas de backup para um cofre de backup.</span><span class="sxs-lookup"><span data-stu-id="9d9a4-103">Gets backup policies for a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d9a4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9d9a4-104">SYNTAX</span></span>

```
Get-AzureRmBackupProtectionPolicy [[-Name] <String>] [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d9a4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9d9a4-105">DESCRIPTION</span></span>
<span data-ttu-id="9d9a4-106">O cmdlet **Get-AzureRmBackupProtectionPolicy** Obtém políticas de backup para um cofre de backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="9d9a4-106">The **Get-AzureRmBackupProtectionPolicy** cmdlet gets backup policies for an Azure Backup vault.</span></span>

## <span data-ttu-id="9d9a4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9d9a4-107">EXAMPLES</span></span>

### <span data-ttu-id="9d9a4-108">Exemplo 1: exibir as políticas em um cofre</span><span class="sxs-lookup"><span data-stu-id="9d9a4-108">Example 1: View the policies in a vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupProtectionPolicy -Vault $Vault 
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
contoso01                 AzureVM            Daily              26-Aug-15 3:00:00 PM
DailyBkp                  AzureVM            Daily              26-Aug-15 3:00:00 PM
DefaultPolicy             AzureVM            Daily              26-Aug-15 12:30:00 AM
WeeklyBkp                 AzureVM            Weekly             26-Aug-15 5:00:00 PM
contoso02                 AzureVM            Daily              26-Aug-15 3:00:00 PM
```

<span data-ttu-id="9d9a4-109">O primeiro comando obtém o cofre chamado Vault03 usando o cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="9d9a4-109">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="9d9a4-110">O comando armazena esse objeto na variável $Vault.</span><span class="sxs-lookup"><span data-stu-id="9d9a4-110">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="9d9a4-111">O segundo comando obtém todas as políticas de proteção de backup para o cofre em $Vault.</span><span class="sxs-lookup"><span data-stu-id="9d9a4-111">The second command gets all the Backup protection policies for the vault in $Vault.</span></span>

### <span data-ttu-id="9d9a4-112">Exemplo 2: obter uma política específica de um cofre</span><span class="sxs-lookup"><span data-stu-id="9d9a4-112">Example 2: Get a specific policy from a vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DefaultPolicy"
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
DefaultPolicy             AzureVM            Daily              26-Aug-15 12:30:00 AM
```

<span data-ttu-id="9d9a4-113">O primeiro comando obtém o cofre chamado Vault03 usando o cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="9d9a4-113">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="9d9a4-114">O comando armazena esse objeto na variável $Vault.</span><span class="sxs-lookup"><span data-stu-id="9d9a4-114">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="9d9a4-115">O segundo comando obtém a política de proteção de backup chamada DefaultPolicy para o cofre em $Vault.</span><span class="sxs-lookup"><span data-stu-id="9d9a4-115">The second command gets the Backup protection policy named DefaultPolicy for the vault in $Vault.</span></span>

## <span data-ttu-id="9d9a4-116">OS</span><span class="sxs-lookup"><span data-stu-id="9d9a4-116">PARAMETERS</span></span>

### <span data-ttu-id="9d9a4-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="9d9a4-117">-Name</span></span>
<span data-ttu-id="9d9a4-118">Especifica o nome da política que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="9d9a4-118">Specifies the name of the policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9d9a4-119">-Cofre</span><span class="sxs-lookup"><span data-stu-id="9d9a4-119">-Vault</span></span>
<span data-ttu-id="9d9a4-120">Especifica o cofre de backup para o qual este cmdlet obtém políticas.</span><span class="sxs-lookup"><span data-stu-id="9d9a4-120">Specifies the Backup vault for which this cmdlet gets policies.</span></span>
<span data-ttu-id="9d9a4-121">Para obter um objeto **AzureRmBackupVault** , use o cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="9d9a4-121">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d9a4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d9a4-122">-DefaultProfile</span></span>
<span data-ttu-id="9d9a4-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9d9a4-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d9a4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d9a4-124">CommonParameters</span></span>
<span data-ttu-id="9d9a4-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d9a4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d9a4-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d9a4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d9a4-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9d9a4-127">INPUTS</span></span>

### <span data-ttu-id="9d9a4-128">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="9d9a4-128">AzureRmBackupVault</span></span>

## <span data-ttu-id="9d9a4-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9d9a4-129">OUTPUTS</span></span>

### <span data-ttu-id="9d9a4-130">AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9d9a4-130">AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="9d9a4-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9d9a4-131">NOTES</span></span>
* <span data-ttu-id="9d9a4-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9d9a4-132">None</span></span>

## <span data-ttu-id="9d9a4-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9d9a4-133">RELATED LINKS</span></span>

[<span data-ttu-id="9d9a4-134">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="9d9a4-134">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="9d9a4-135">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="9d9a4-135">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="9d9a4-136">New-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9d9a4-136">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="9d9a4-137">Remove-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9d9a4-137">Remove-AzureRmBackupProtectionPolicy</span></span>](./Remove-AzureRmBackupProtectionPolicy.md)


