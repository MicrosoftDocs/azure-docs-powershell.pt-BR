---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 4750561aed6643c17fed6e42d13551be76635d72
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433707"
---
# <span data-ttu-id="d9eaf-101">Restore-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d9eaf-101">Restore-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="d9eaf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d9eaf-102">SYNOPSIS</span></span>
<span data-ttu-id="d9eaf-103">Restaura uma conta de armazenamento gerenciado em um cofre de chaves de um arquivo de backup.</span><span class="sxs-lookup"><span data-stu-id="d9eaf-103">Restores a managed storage account in a key vault from a backup file.</span></span>

## <span data-ttu-id="d9eaf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9eaf-104">SYNTAX</span></span>

### <span data-ttu-id="d9eaf-105">ByVaultName (padrão)</span><span class="sxs-lookup"><span data-stu-id="d9eaf-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9eaf-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d9eaf-106">ByInputObject</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9eaf-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d9eaf-107">ByResourceId</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9eaf-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d9eaf-108">DESCRIPTION</span></span>
<span data-ttu-id="d9eaf-109">O cmdlet **Restore-AzKeyVaultManagedStorageAccount** cria uma conta de armazenamento gerenciado no cofre de chaves especificado a partir de um arquivo de backup.</span><span class="sxs-lookup"><span data-stu-id="d9eaf-109">The **Restore-AzKeyVaultManagedStorageAccount** cmdlet creates a managed storage account in the specified key vault from a backup file.</span></span>
<span data-ttu-id="d9eaf-110">Esta conta de armazenamento gerenciado é uma réplica da conta de armazenamento gerenciado com backup no arquivo de entrada e tem o mesmo nome do original.</span><span class="sxs-lookup"><span data-stu-id="d9eaf-110">This managed storage account is a replica of the backed-up managed storage account in the input file and has the same name as the original.</span></span>
<span data-ttu-id="d9eaf-111">Se o cofre de chaves já contiver uma conta de armazenamento gerenciado com o mesmo nome, esse cmdlet falha em vez de substituir o original.</span><span class="sxs-lookup"><span data-stu-id="d9eaf-111">If the key vault already contains a managed storage account by the same name, this cmdlet fails instead of overwriting the original.</span></span>
<span data-ttu-id="d9eaf-112">O cofre de chaves para o qual você restaura a conta de armazenamento gerenciada pode ser diferente do cofre de chaves do qual você tem o backup da conta de armazenamento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="d9eaf-112">The key vault that you restore the managed storage account into can be different from the key vault that you backed up the managed storage account from.</span></span>
<span data-ttu-id="d9eaf-113">No entanto, o cofre de chaves deve usar a mesma assinatura e estar em uma região do Azure na mesma Geografia (por exemplo, América do Norte).</span><span class="sxs-lookup"><span data-stu-id="d9eaf-113">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="d9eaf-114">Consulte a central de confiabilidade do Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) para o mapeamento de regiões do Azure para regiões geográficas.</span><span class="sxs-lookup"><span data-stu-id="d9eaf-114">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="d9eaf-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d9eaf-115">EXAMPLES</span></span>

### <span data-ttu-id="d9eaf-116">Exemplo 1: restaurar uma conta de armazenamento gerenciado com backup</span><span class="sxs-lookup"><span data-stu-id="d9eaf-116">Example 1: Restore a backed-up managed storage account</span></span>
```powershell
PS C:\> Restore-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

Id                  : https://mykeyvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : MyKeyVault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key1
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="d9eaf-117">Esse comando restaura uma conta de armazenamento gerenciado, incluindo todas as suas versões, do arquivo de backup chamado backup. blob no cofre de chaves chamado MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="d9eaf-117">This command restores a managed storage account, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="d9eaf-118">OS</span><span class="sxs-lookup"><span data-stu-id="d9eaf-118">PARAMETERS</span></span>

### <span data-ttu-id="d9eaf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9eaf-119">-DefaultProfile</span></span>
<span data-ttu-id="d9eaf-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d9eaf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9eaf-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="d9eaf-121">-InputFile</span></span>
<span data-ttu-id="d9eaf-122">Arquivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="d9eaf-122">Input file.</span></span>
<span data-ttu-id="d9eaf-123">O arquivo de entrada que contém o blob com backup</span><span class="sxs-lookup"><span data-stu-id="d9eaf-123">The input file containing the backed-up blob</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9eaf-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9eaf-124">-InputObject</span></span>
<span data-ttu-id="d9eaf-125">Objeto do keyvault</span><span class="sxs-lookup"><span data-stu-id="d9eaf-125">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9eaf-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9eaf-126">-ResourceId</span></span>
<span data-ttu-id="d9eaf-127">ID do recurso do keyvault</span><span class="sxs-lookup"><span data-stu-id="d9eaf-127">KeyVault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9eaf-128">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="d9eaf-128">-VaultName</span></span>
<span data-ttu-id="d9eaf-129">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="d9eaf-129">Vault name.</span></span>
<span data-ttu-id="d9eaf-130">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="d9eaf-130">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9eaf-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d9eaf-131">-Confirm</span></span>
<span data-ttu-id="d9eaf-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9eaf-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9eaf-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9eaf-133">-WhatIf</span></span>
<span data-ttu-id="d9eaf-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d9eaf-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9eaf-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d9eaf-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9eaf-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9eaf-136">CommonParameters</span></span>
<span data-ttu-id="d9eaf-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9eaf-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9eaf-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9eaf-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9eaf-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d9eaf-139">INPUTS</span></span>

### <span data-ttu-id="d9eaf-140">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="d9eaf-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="d9eaf-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d9eaf-141">System.String</span></span>

## <span data-ttu-id="d9eaf-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d9eaf-142">OUTPUTS</span></span>

### <span data-ttu-id="d9eaf-143">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d9eaf-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="d9eaf-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d9eaf-144">NOTES</span></span>

## <span data-ttu-id="d9eaf-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d9eaf-145">RELATED LINKS</span></span>
