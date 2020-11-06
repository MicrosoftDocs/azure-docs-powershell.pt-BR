---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 015E3BC9-C535-4EA2-8A30-C728385DBFF8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/new-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupVault.md
ms.openlocfilehash: 77c2df1ec61b42aaded458bea564cf6c953c90ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432954"
---
# <span data-ttu-id="77c5f-101">New-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="77c5f-101">New-AzureRmBackupVault</span></span>

## <span data-ttu-id="77c5f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="77c5f-102">SYNOPSIS</span></span>
<span data-ttu-id="77c5f-103">Cria um cofre de backup.</span><span class="sxs-lookup"><span data-stu-id="77c5f-103">Creates a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77c5f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="77c5f-104">SYNTAX</span></span>

```
New-AzureRmBackupVault [-ResourceGroupName] <String> [-Name] <String> [-Region] <String>
 [[-Storage] <AzureBackupVaultStorageType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77c5f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="77c5f-105">DESCRIPTION</span></span>
<span data-ttu-id="77c5f-106">O cmdlet **New-AzureRmBackupVault** cria um cofre de backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="77c5f-106">The **New-AzureRmBackupVault** cmdlet creates an Azure Backup vault.</span></span>
<span data-ttu-id="77c5f-107">Esse cmdlet retorna um objeto **AzureRmBackupVault** que atua como uma referência à entidade do cofre.</span><span class="sxs-lookup"><span data-stu-id="77c5f-107">This cmdlet returns an **AzureRmBackupVault** object that acts as a reference to the vault entity.</span></span>

## <span data-ttu-id="77c5f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="77c5f-108">EXAMPLES</span></span>

### <span data-ttu-id="77c5f-109">Exemplo 1: criar um cofre de backup</span><span class="sxs-lookup"><span data-stu-id="77c5f-109">Example 1: Create a backup vault</span></span>
```
PS C:\>New-AzureRmBackupVault -ResourceGroupName "ResourceGroup01" -Name "Vault03" -Region "westus"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup01/providers/Microsoft.Backup
                    /BackupVault/Vault03
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

<span data-ttu-id="77c5f-110">Esse comando cria um cofre de backup do Azure chamado Vault03.</span><span class="sxs-lookup"><span data-stu-id="77c5f-110">This command creates an Azure Backup vault named Vault03.</span></span>
<span data-ttu-id="77c5f-111">O cofre está no grupo de recursos chamado ResourceGroup01 na região oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="77c5f-111">The vault is in the resource group named ResourceGroup01 in the West US region.</span></span>
<span data-ttu-id="77c5f-112">O cofre usa o tipo de armazenamento georedundante padrão.</span><span class="sxs-lookup"><span data-stu-id="77c5f-112">The vault uses the default GeoRedundant storage type.</span></span>

### <span data-ttu-id="77c5f-113">Exemplo 2: criar um cofre de backup que usa armazenamento redundante localmente</span><span class="sxs-lookup"><span data-stu-id="77c5f-113">Example 2: Create a backup vault that uses locally redundant storage</span></span>
```
PS C:\>New-AzureRmBackupVault -ResourceGroupName "ResourceGroup02" -Name "Vault03" -Region "westus" -Storage LocallyRedundant
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup02/providers/Microsoft.Backup
                    /BackupVault/Vault03
Name              : Vault03
ResourceGroupName : ResourceGroup02
Region            : westus
Storage           : LocallyRedundant
```

<span data-ttu-id="77c5f-114">Esse comando cria um cofre de backup do Azure chamado Vault03.</span><span class="sxs-lookup"><span data-stu-id="77c5f-114">This command creates an Azure Backup vault named Vault03.</span></span>
<span data-ttu-id="77c5f-115">O cofre está no grupo de recursos chamado ResourceGroup02 na região oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="77c5f-115">The vault is in the resource group named ResourceGroup02 in the West US region.</span></span>
<span data-ttu-id="77c5f-116">O cofre usa o tipo de armazenamento LocallyRedundant.</span><span class="sxs-lookup"><span data-stu-id="77c5f-116">The vault uses the LocallyRedundant storage type.</span></span>

## <span data-ttu-id="77c5f-117">OS</span><span class="sxs-lookup"><span data-stu-id="77c5f-117">PARAMETERS</span></span>

### <span data-ttu-id="77c5f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77c5f-118">-DefaultProfile</span></span>
<span data-ttu-id="77c5f-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="77c5f-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77c5f-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="77c5f-120">-Name</span></span>
<span data-ttu-id="77c5f-121">Especifica um nome para o cofre de backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="77c5f-121">Specifies a name for the Azure Backup vault.</span></span>
<span data-ttu-id="77c5f-122">O nome deve ser exclusivo em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="77c5f-122">The name must be unique in a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77c5f-123">-Região</span><span class="sxs-lookup"><span data-stu-id="77c5f-123">-Region</span></span>
<span data-ttu-id="77c5f-124">Especifica uma região do Azure na qual existe o cofre de backup.</span><span class="sxs-lookup"><span data-stu-id="77c5f-124">Specifies an Azure region in which the backup vault exists.</span></span>
<span data-ttu-id="77c5f-125">Para cenários de backup híbrido, recomendamos que você crie um cofre em uma região perto do servidor local para reduzir a latência.</span><span class="sxs-lookup"><span data-stu-id="77c5f-125">For hybrid backup scenarios, we recommend that you create a vault in a region close to the on-premise server to reduce latency.</span></span>
<span data-ttu-id="77c5f-126">Para fazer backup de máquinas virtuais do Microsoft Azure infraestrutura como serviço (IaaS), o cofre se torna o ponto de descoberta para máquinas virtuais locais.</span><span class="sxs-lookup"><span data-stu-id="77c5f-126">For backup of Azure infrastructure as a service (IaaS) virtual machines, the vault becomes the point of discovery for local virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77c5f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77c5f-127">-ResourceGroupName</span></span>
<span data-ttu-id="77c5f-128">Especifica o nome de um grupo de recursos do Azure existente no qual esse cmdlet cria um cofre de backup.</span><span class="sxs-lookup"><span data-stu-id="77c5f-128">Specifies the name of an existing Azure resource group in which this cmdlet creates a Backup vault.</span></span>
<span data-ttu-id="77c5f-129">Para criar um grupo de recursos, use o cmdlet New-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="77c5f-129">To create a resource group, use the New-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="77c5f-130">O grupo de recursos e o cofre de backup do Azure não precisam estar na mesma região.</span><span class="sxs-lookup"><span data-stu-id="77c5f-130">The resource group and the Azure Backup vault do not have to be in the same region.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77c5f-131">-Armazenamento</span><span class="sxs-lookup"><span data-stu-id="77c5f-131">-Storage</span></span>
<span data-ttu-id="77c5f-132">Especifica o tipo de armazenamento dos dados de backup.</span><span class="sxs-lookup"><span data-stu-id="77c5f-132">Specifies the storage type for the backup data.</span></span>
<span data-ttu-id="77c5f-133">Os valores aceitáveis para esse parâmetro são: LocallyRedundant e georedundantes.</span><span class="sxs-lookup"><span data-stu-id="77c5f-133">The acceptable values for this parameter are: LocallyRedundant and GeoRedundant.</span></span>
<span data-ttu-id="77c5f-134">O valor padrão é georedundante.</span><span class="sxs-lookup"><span data-stu-id="77c5f-134">The default value is GeoRedundant.</span></span>

```yaml
Type: AzureBackupVaultStorageType
Parameter Sets: (All)
Aliases: 
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77c5f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77c5f-135">CommonParameters</span></span>
<span data-ttu-id="77c5f-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77c5f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77c5f-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77c5f-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77c5f-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="77c5f-138">INPUTS</span></span>

### <span data-ttu-id="77c5f-139">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="77c5f-139">None</span></span>

## <span data-ttu-id="77c5f-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="77c5f-140">OUTPUTS</span></span>

### <span data-ttu-id="77c5f-141">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="77c5f-141">AzureRmBackupVault</span></span>

## <span data-ttu-id="77c5f-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="77c5f-142">NOTES</span></span>
* <span data-ttu-id="77c5f-143">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="77c5f-143">None</span></span>

## <span data-ttu-id="77c5f-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="77c5f-144">RELATED LINKS</span></span>

[<span data-ttu-id="77c5f-145">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="77c5f-145">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="77c5f-146">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="77c5f-146">Remove-AzureRmBackupVault</span></span>](./Remove-AzureRmBackupVault.md)

[<span data-ttu-id="77c5f-147">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="77c5f-147">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)


