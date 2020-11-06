---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: D57C32D1-EB4F-495E-A11B-3B4066E8C552
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/set-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupVault.md
ms.openlocfilehash: edb119484d397241b786ff9476b688e150ed3c6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428596"
---
# <span data-ttu-id="8993f-101">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="8993f-101">Set-AzureRmBackupVault</span></span>

## <span data-ttu-id="8993f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8993f-102">SYNOPSIS</span></span>
<span data-ttu-id="8993f-103">Altera o tipo de armazenamento de um cofre de backup.</span><span class="sxs-lookup"><span data-stu-id="8993f-103">Changes the storage type of a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8993f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8993f-104">SYNTAX</span></span>

```
Set-AzureRmBackupVault [[-Storage] <AzureBackupVaultStorageType>] [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8993f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8993f-105">DESCRIPTION</span></span>
<span data-ttu-id="8993f-106">O cmdlet **set-AzureRmBackupVault** altera o tipo de armazenamento de um cofre de backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="8993f-106">The **Set-AzureRmBackupVault** cmdlet changes the storage type of an Azure Backup vault.</span></span>
<span data-ttu-id="8993f-107">Não é possível modificar outras propriedades de um cofre.</span><span class="sxs-lookup"><span data-stu-id="8993f-107">You cannot modify other properties of a vault.</span></span>

## <span data-ttu-id="8993f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8993f-108">EXAMPLES</span></span>

### <span data-ttu-id="8993f-109">Exemplo 1: alterar o armazenamento de um cofre existente</span><span class="sxs-lookup"><span data-stu-id="8993f-109">Example 1: Change the storage for an existing vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03" | Set-AzureRmBackupVault -Storage LocallyRedundant
```

<span data-ttu-id="8993f-110">Esse comando obtém o cofre de backup do Azure chamado Vault03 usando o cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="8993f-110">This command gets the Azure Backup vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="8993f-111">O comando passa o cofre para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="8993f-111">The command passes that vault to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8993f-112">O cmdlet atual altera o tipo de armazenamento para LocallyRedundant.</span><span class="sxs-lookup"><span data-stu-id="8993f-112">The current cmdlet changes the storage type to LocallyRedundant.</span></span>

## <span data-ttu-id="8993f-113">OS</span><span class="sxs-lookup"><span data-stu-id="8993f-113">PARAMETERS</span></span>

### <span data-ttu-id="8993f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8993f-114">-DefaultProfile</span></span>
<span data-ttu-id="8993f-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8993f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8993f-116">-Armazenamento</span><span class="sxs-lookup"><span data-stu-id="8993f-116">-Storage</span></span>
<span data-ttu-id="8993f-117">Especifica o tipo de armazenamento dos dados de backup.</span><span class="sxs-lookup"><span data-stu-id="8993f-117">Specifies the storage type for the backup data.</span></span>
<span data-ttu-id="8993f-118">Os valores aceitáveis para esse parâmetro são: LocallyRedundant e georedundantes.</span><span class="sxs-lookup"><span data-stu-id="8993f-118">The acceptable values for this parameter are: LocallyRedundant and GeoRedundant.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupVaultStorageType
Parameter Sets: (All)
Aliases:
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8993f-119">-Cofre</span><span class="sxs-lookup"><span data-stu-id="8993f-119">-Vault</span></span>
<span data-ttu-id="8993f-120">Especifica um cofre de backup que é modificado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8993f-120">Specifies a Backup vault that this cmdlet modifies.</span></span>
<span data-ttu-id="8993f-121">Para obter um objeto **AzureRmBackupVault** , use o cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="8993f-121">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="8993f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8993f-122">CommonParameters</span></span>
<span data-ttu-id="8993f-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8993f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8993f-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8993f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8993f-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8993f-125">INPUTS</span></span>

### <span data-ttu-id="8993f-126">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="8993f-126">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>
<span data-ttu-id="8993f-127">Parâmetros: cofre (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8993f-127">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="8993f-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8993f-128">OUTPUTS</span></span>

### <span data-ttu-id="8993f-129">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="8993f-129">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>

## <span data-ttu-id="8993f-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8993f-130">NOTES</span></span>
* <span data-ttu-id="8993f-131">Quando você registra o primeiro servidor ou máquina virtual para um cofre, o tipo de armazenamento fica bloqueado.</span><span class="sxs-lookup"><span data-stu-id="8993f-131">When you register the first server or virtual machine for a vault, the storage type is locked.</span></span> <span data-ttu-id="8993f-132">Em seguida, você não pode alterar o tipo de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8993f-132">Subsequently, you cannot change the storage type.</span></span>

## <span data-ttu-id="8993f-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8993f-133">RELATED LINKS</span></span>

[<span data-ttu-id="8993f-134">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="8993f-134">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="8993f-135">New-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="8993f-135">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="8993f-136">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="8993f-136">Remove-AzureRmBackupVault</span></span>](./Remove-AzureRmBackupVault.md)


