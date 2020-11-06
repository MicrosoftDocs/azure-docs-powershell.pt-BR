---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: D57C32D1-EB4F-495E-A11B-3B4066E8C552
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupVault.md
ms.openlocfilehash: 82e86d27c5ef628e6cd6122fa024ac72788e79db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432673"
---
# <span data-ttu-id="65ee0-101">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="65ee0-101">Set-AzureRmBackupVault</span></span>

## <span data-ttu-id="65ee0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="65ee0-102">SYNOPSIS</span></span>
<span data-ttu-id="65ee0-103">Altera o tipo de armazenamento de um cofre de backup.</span><span class="sxs-lookup"><span data-stu-id="65ee0-103">Changes the storage type of a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65ee0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="65ee0-104">SYNTAX</span></span>

```
Set-AzureRmBackupVault [[-Storage] <AzureBackupVaultStorageType>] [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65ee0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="65ee0-105">DESCRIPTION</span></span>
<span data-ttu-id="65ee0-106">O cmdlet **set-AzureRmBackupVault** altera o tipo de armazenamento de um cofre de backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="65ee0-106">The **Set-AzureRmBackupVault** cmdlet changes the storage type of an Azure Backup vault.</span></span>
<span data-ttu-id="65ee0-107">Não é possível modificar outras propriedades de um cofre.</span><span class="sxs-lookup"><span data-stu-id="65ee0-107">You cannot modify other properties of a vault.</span></span>

## <span data-ttu-id="65ee0-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="65ee0-108">EXAMPLES</span></span>

### <span data-ttu-id="65ee0-109">Exemplo 1: alterar o armazenamento de um cofre existente</span><span class="sxs-lookup"><span data-stu-id="65ee0-109">Example 1: Change the storage for an existing vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03" | Set-AzureRmBackupVault -Storage LocallyRedundant
```

<span data-ttu-id="65ee0-110">Esse comando obtém o cofre de backup do Azure chamado Vault03 usando o cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="65ee0-110">This command gets the Azure Backup vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="65ee0-111">O comando passa o cofre para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="65ee0-111">The command passes that vault to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="65ee0-112">O cmdlet atual altera o tipo de armazenamento para LocallyRedundant.</span><span class="sxs-lookup"><span data-stu-id="65ee0-112">The current cmdlet changes the storage type to LocallyRedundant.</span></span>

## <span data-ttu-id="65ee0-113">OS</span><span class="sxs-lookup"><span data-stu-id="65ee0-113">PARAMETERS</span></span>

### <span data-ttu-id="65ee0-114">-Armazenamento</span><span class="sxs-lookup"><span data-stu-id="65ee0-114">-Storage</span></span>
<span data-ttu-id="65ee0-115">Especifica o tipo de armazenamento dos dados de backup.</span><span class="sxs-lookup"><span data-stu-id="65ee0-115">Specifies the storage type for the backup data.</span></span>
<span data-ttu-id="65ee0-116">Os valores aceitáveis para esse parâmetro são: LocallyRedundant e georedundantes.</span><span class="sxs-lookup"><span data-stu-id="65ee0-116">The acceptable values for this parameter are: LocallyRedundant and GeoRedundant.</span></span>

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

### <span data-ttu-id="65ee0-117">-Cofre</span><span class="sxs-lookup"><span data-stu-id="65ee0-117">-Vault</span></span>
<span data-ttu-id="65ee0-118">Especifica um cofre de backup que é modificado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65ee0-118">Specifies a Backup vault that this cmdlet modifies.</span></span>
<span data-ttu-id="65ee0-119">Para obter um objeto **AzureRmBackupVault** , use o cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="65ee0-119">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="65ee0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65ee0-120">-DefaultProfile</span></span>
<span data-ttu-id="65ee0-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="65ee0-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65ee0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65ee0-122">CommonParameters</span></span>
<span data-ttu-id="65ee0-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65ee0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65ee0-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65ee0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65ee0-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="65ee0-125">INPUTS</span></span>

### <span data-ttu-id="65ee0-126">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="65ee0-126">AzureRmBackupVault</span></span>

## <span data-ttu-id="65ee0-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="65ee0-127">OUTPUTS</span></span>

### <span data-ttu-id="65ee0-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="65ee0-128">None</span></span>

## <span data-ttu-id="65ee0-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="65ee0-129">NOTES</span></span>
* <span data-ttu-id="65ee0-130">Quando você registra o primeiro servidor ou máquina virtual para um cofre, o tipo de armazenamento fica bloqueado.</span><span class="sxs-lookup"><span data-stu-id="65ee0-130">When you register the first server or virtual machine for a vault, the storage type is locked.</span></span> <span data-ttu-id="65ee0-131">Em seguida, você não pode alterar o tipo de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="65ee0-131">Subsequently, you cannot change the storage type.</span></span>

## <span data-ttu-id="65ee0-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65ee0-132">RELATED LINKS</span></span>

[<span data-ttu-id="65ee0-133">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="65ee0-133">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="65ee0-134">New-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="65ee0-134">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="65ee0-135">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="65ee0-135">Remove-AzureRmBackupVault</span></span>](./Remove-AzureRmBackupVault.md)


