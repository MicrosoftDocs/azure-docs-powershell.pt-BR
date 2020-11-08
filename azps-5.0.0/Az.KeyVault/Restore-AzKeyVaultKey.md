---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
ms.openlocfilehash: 17a39152c6e341773a2c3db7b701e0d37890f110
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115287"
---
# <span data-ttu-id="76537-101">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="76537-101">Restore-AzKeyVaultKey</span></span>

## <span data-ttu-id="76537-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="76537-102">SYNOPSIS</span></span>
<span data-ttu-id="76537-103">Cria uma chave em um cofre de chaves de uma chave com backup.</span><span class="sxs-lookup"><span data-stu-id="76537-103">Creates a key in a key vault from a backed-up key.</span></span>

## <span data-ttu-id="76537-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76537-104">SYNTAX</span></span>

### <span data-ttu-id="76537-105">ByVaultName (padrão)</span><span class="sxs-lookup"><span data-stu-id="76537-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76537-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="76537-106">ByInputObject</span></span>
```
Restore-AzKeyVaultKey [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76537-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="76537-107">ByResourceId</span></span>
```
Restore-AzKeyVaultKey [-ResourceId] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76537-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="76537-108">DESCRIPTION</span></span>
<span data-ttu-id="76537-109">O cmdlet **Restore-AzKeyVaultKey** cria uma chave no cofre de chaves especificado.</span><span class="sxs-lookup"><span data-stu-id="76537-109">The **Restore-AzKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="76537-110">Essa chave é uma réplica da chave com backup no arquivo de entrada e tem o mesmo nome da chave original.</span><span class="sxs-lookup"><span data-stu-id="76537-110">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="76537-111">Se o cofre de chaves já tiver uma chave com o mesmo nome, esse cmdlet falha em vez de substituir a chave original.</span><span class="sxs-lookup"><span data-stu-id="76537-111">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="76537-112">Se o backup contiver várias versões de uma chave, todas as versões serão restauradas.</span><span class="sxs-lookup"><span data-stu-id="76537-112">If the backup contains multiple versions of a key, all versions are restored.</span></span>
<span data-ttu-id="76537-113">O cofre de chaves no qual você restaura a chave pode ser diferente do cofre de chaves do qual você tem o backup da chave.</span><span class="sxs-lookup"><span data-stu-id="76537-113">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="76537-114">No entanto, o cofre de chaves deve usar a mesma assinatura e estar em uma região do Azure na mesma Geografia (por exemplo, América do Norte).</span><span class="sxs-lookup"><span data-stu-id="76537-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="76537-115">Consulte a central de confiabilidade do Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) para o mapeamento de regiões do Azure para regiões geográficas.</span><span class="sxs-lookup"><span data-stu-id="76537-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="76537-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="76537-116">EXAMPLES</span></span>

### <span data-ttu-id="76537-117">Exemplo 1: restaurar uma chave de backup</span><span class="sxs-lookup"><span data-stu-id="76537-117">Example 1: Restore a backed-up key</span></span>
```powershell
PS C:\> Restore-AzKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

Vault Name     : MyKeyVault
Name           : key1
Version        : 394f9379a47a4e2086585468de6c7ae5
Id             : https://mykeyvault.vault.azure.net:443/keys/key1/394f9379a47a4e2086585468de6c7ae5
Enabled        : True
Expires        :
Not Before     :
Created        : 4/6/2018 11:31:36 PM
Updated        : 4/6/2018 11:35:04 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="76537-118">Esse comando restaura uma chave, incluindo todas as suas versões, do arquivo de backup chamado backup. blob no cofre de chaves chamado MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="76537-118">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="76537-119">OS</span><span class="sxs-lookup"><span data-stu-id="76537-119">PARAMETERS</span></span>

### <span data-ttu-id="76537-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76537-120">-DefaultProfile</span></span>
<span data-ttu-id="76537-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="76537-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76537-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="76537-122">-InputFile</span></span>
<span data-ttu-id="76537-123">Especifica o arquivo de entrada que contém o backup da chave a ser restaurada.</span><span class="sxs-lookup"><span data-stu-id="76537-123">Specifies the input file that contains the backup of the key to restore.</span></span>

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

### <span data-ttu-id="76537-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76537-124">-InputObject</span></span>
<span data-ttu-id="76537-125">Objeto do keyvault</span><span class="sxs-lookup"><span data-stu-id="76537-125">KeyVault object</span></span>

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

### <span data-ttu-id="76537-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76537-126">-ResourceId</span></span>
<span data-ttu-id="76537-127">ID do recurso do keyvault</span><span class="sxs-lookup"><span data-stu-id="76537-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="76537-128">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="76537-128">-VaultName</span></span>
<span data-ttu-id="76537-129">Especifica o nome do cofre de chaves no qual a chave será restaurada.</span><span class="sxs-lookup"><span data-stu-id="76537-129">Specifies the name of the key vault into which to restore the key.</span></span>

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

### <span data-ttu-id="76537-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="76537-130">-Confirm</span></span>
<span data-ttu-id="76537-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76537-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76537-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76537-132">-WhatIf</span></span>
<span data-ttu-id="76537-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="76537-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76537-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="76537-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76537-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76537-135">CommonParameters</span></span>
<span data-ttu-id="76537-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76537-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76537-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76537-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76537-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="76537-138">INPUTS</span></span>

### <span data-ttu-id="76537-139">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="76537-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="76537-140">System. String</span><span class="sxs-lookup"><span data-stu-id="76537-140">System.String</span></span>

## <span data-ttu-id="76537-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="76537-141">OUTPUTS</span></span>

### <span data-ttu-id="76537-142">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="76537-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="76537-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="76537-143">NOTES</span></span>

## <span data-ttu-id="76537-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76537-144">RELATED LINKS</span></span>

[<span data-ttu-id="76537-145">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="76537-145">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="76537-146">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="76537-146">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="76537-147">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="76537-147">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="76537-148">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="76537-148">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

