---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/restore-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 136469819a43dbb918aefebd8134b38ef4a943c7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885445"
---
# <span data-ttu-id="6f27c-101">Restore-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6f27c-101">Restore-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="6f27c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f27c-102">SYNOPSIS</span></span>
<span data-ttu-id="6f27c-103">Restaura uma conta de armazenamento gerenciado em um cofre de chaves de um arquivo de backup.</span><span class="sxs-lookup"><span data-stu-id="6f27c-103">Restores a managed storage account in a key vault from a backup file.</span></span>

## <span data-ttu-id="6f27c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6f27c-104">SYNTAX</span></span>

### <span data-ttu-id="6f27c-105">ByVaultName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6f27c-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f27c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6f27c-106">ByInputObject</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f27c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6f27c-107">ByResourceId</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f27c-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6f27c-108">DESCRIPTION</span></span>
<span data-ttu-id="6f27c-109">O cmdlet **Restore-AzKeyVaultManagedStorageAccount** cria uma conta de armazenamento gerenciado no cofre de chaves especificado de um arquivo de backup.</span><span class="sxs-lookup"><span data-stu-id="6f27c-109">The **Restore-AzKeyVaultManagedStorageAccount** cmdlet creates a managed storage account in the specified key vault from a backup file.</span></span>
<span data-ttu-id="6f27c-110">Essa conta de armazenamento gerenciado é uma réplica da conta de armazenamento gerenciado com backup no arquivo de entrada e tem o mesmo nome do original.</span><span class="sxs-lookup"><span data-stu-id="6f27c-110">This managed storage account is a replica of the backed-up managed storage account in the input file and has the same name as the original.</span></span>
<span data-ttu-id="6f27c-111">Se o cofre de chaves já contiver uma conta de armazenamento gerenciada pelo mesmo nome, esse cmdlet falhará em vez de sobrescrever o original.</span><span class="sxs-lookup"><span data-stu-id="6f27c-111">If the key vault already contains a managed storage account by the same name, this cmdlet fails instead of overwriting the original.</span></span>
<span data-ttu-id="6f27c-112">O cofre de chaves em que você restaura a conta de armazenamento gerenciado pode ser diferente do cofre de chaves do que você fez o backup da conta de armazenamento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="6f27c-112">The key vault that you restore the managed storage account into can be different from the key vault that you backed up the managed storage account from.</span></span>
<span data-ttu-id="6f27c-113">No entanto, o cofre de chaves deve usar a mesma assinatura e estar em uma região do Azure na mesma geografia (por exemplo, América do Norte).</span><span class="sxs-lookup"><span data-stu-id="6f27c-113">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="6f27c-114">Consulte o Centro de Confiança do Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) para o mapeamento de regiões do Azure para geografias.</span><span class="sxs-lookup"><span data-stu-id="6f27c-114">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="6f27c-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6f27c-115">EXAMPLES</span></span>

### <span data-ttu-id="6f27c-116">Exemplo 1: Restaurar uma conta de armazenamento gerenciado com backup</span><span class="sxs-lookup"><span data-stu-id="6f27c-116">Example 1: Restore a backed-up managed storage account</span></span>
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

<span data-ttu-id="6f27c-117">Este comando restaura uma conta de armazenamento gerenciado, incluindo todas as suas versões, do arquivo de backup chamado Backup.blob para o cofre de chaves chamado MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="6f27c-117">This command restores a managed storage account, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="6f27c-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6f27c-118">PARAMETERS</span></span>

### <span data-ttu-id="6f27c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f27c-119">-DefaultProfile</span></span>
<span data-ttu-id="6f27c-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6f27c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f27c-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="6f27c-121">-InputFile</span></span>
<span data-ttu-id="6f27c-122">Arquivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="6f27c-122">Input file.</span></span>
<span data-ttu-id="6f27c-123">O arquivo de entrada que contém o blob de backup</span><span class="sxs-lookup"><span data-stu-id="6f27c-123">The input file containing the backed-up blob</span></span>

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

### <span data-ttu-id="6f27c-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f27c-124">-InputObject</span></span>
<span data-ttu-id="6f27c-125">Objeto KeyVault</span><span class="sxs-lookup"><span data-stu-id="6f27c-125">KeyVault object</span></span>

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

### <span data-ttu-id="6f27c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f27c-126">-ResourceId</span></span>
<span data-ttu-id="6f27c-127">ID do Recurso KeyVault</span><span class="sxs-lookup"><span data-stu-id="6f27c-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="6f27c-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="6f27c-128">-VaultName</span></span>
<span data-ttu-id="6f27c-129">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="6f27c-129">Vault name.</span></span>
<span data-ttu-id="6f27c-130">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="6f27c-130">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="6f27c-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6f27c-131">-Confirm</span></span>
<span data-ttu-id="6f27c-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f27c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f27c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f27c-133">-WhatIf</span></span>
<span data-ttu-id="6f27c-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6f27c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f27c-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6f27c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f27c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f27c-136">CommonParameters</span></span>
<span data-ttu-id="6f27c-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f27c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f27c-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f27c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f27c-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6f27c-139">INPUTS</span></span>

### <span data-ttu-id="6f27c-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="6f27c-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="6f27c-141">System.String</span><span class="sxs-lookup"><span data-stu-id="6f27c-141">System.String</span></span>

## <span data-ttu-id="6f27c-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6f27c-142">OUTPUTS</span></span>

### <span data-ttu-id="6f27c-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6f27c-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="6f27c-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="6f27c-144">NOTES</span></span>

## <span data-ttu-id="6f27c-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6f27c-145">RELATED LINKS</span></span>
