---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmKey.md
ms.openlocfilehash: 9e75b6de483f0103103434518d31b472660f4a70
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280506"
---
# <span data-ttu-id="11630-101">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="11630-101">Backup-AzManagedHsmKey</span></span>

## <span data-ttu-id="11630-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="11630-102">SYNOPSIS</span></span>
<span data-ttu-id="11630-103">Faz backup de uma chave em um HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="11630-103">Backs up a key in a managed HSM.</span></span>

## <span data-ttu-id="11630-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="11630-104">SYNTAX</span></span>

### <span data-ttu-id="11630-105">ByKeyName (padrão)</span><span class="sxs-lookup"><span data-stu-id="11630-105">ByKeyName (Default)</span></span>
```
Backup-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11630-106">ByKey</span><span class="sxs-lookup"><span data-stu-id="11630-106">ByKey</span></span>
```
Backup-AzManagedHsmKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11630-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="11630-107">DESCRIPTION</span></span>
<span data-ttu-id="11630-108">O cmdlet **backup-AzManagedHsmKey** faz backup de uma chave especificada em um HSM gerenciado, baixando-a e armazenando-a em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="11630-108">The **Backup-AzManagedHsmKey** cmdlet backs up a specified key in a managed HSM by downloading it and storing it in a file.</span></span>
<span data-ttu-id="11630-109">Se houver várias versões da chave, todas as versões serão incluídas no backup.</span><span class="sxs-lookup"><span data-stu-id="11630-109">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="11630-110">Como o conteúdo baixado é criptografado, ele não pode ser usado fora do Azure Managed HSM.</span><span class="sxs-lookup"><span data-stu-id="11630-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Managed HSM.</span></span>
<span data-ttu-id="11630-111">Você pode restaurar uma chave em backup para qualquer HSM gerenciado na assinatura da qual foi feito o backup.</span><span class="sxs-lookup"><span data-stu-id="11630-111">You can restore a backed-up key to any managed HSM in the subscription that it was backed up from.</span></span>
<span data-ttu-id="11630-112">Os motivos típicos para usar este cmdlet são:</span><span class="sxs-lookup"><span data-stu-id="11630-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="11630-113">Você deseja fazer a caução de uma cópia da sua chave para que tenha uma cópia offline em caso de excluir acidentalmente a chave no HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="11630-113">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your managed HSM.</span></span>
 
- <span data-ttu-id="11630-114">Você criou uma chave usando HSM gerenciado e agora deseja clonar a chave em uma região diferente do Azure, de modo que você possa usá-la em todas as instâncias do seu aplicativo distribuído.</span><span class="sxs-lookup"><span data-stu-id="11630-114">You created a key using Managed HSM and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="11630-115">Use o cmdlet **backup-AzManagedHsmKey** para recuperar a chave no formato criptografado e, em seguida, use o cmdlet Restore-AzManagedHsmKey e ESPECIFIQUE um HSM gerenciado na segunda região.</span><span class="sxs-lookup"><span data-stu-id="11630-115">Use the **Backup-AzManagedHsmKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzManagedHsmKey cmdlet and specify a managed HSM in the second region.</span></span>

## <span data-ttu-id="11630-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="11630-116">EXAMPLES</span></span>

### <span data-ttu-id="11630-117">Exemplo 1: fazer backup de uma chave com um nome de arquivo gerado automaticamente</span><span class="sxs-lookup"><span data-stu-id="11630-117">Example 1: Back up a key with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzManagedHsmKey -HsmName testmhsm -Name testkey

C:\Users\username\testmhsm-testkey-1602664728.7106073
```

<span data-ttu-id="11630-118">Esse comando recupera a chave chamada TestKey do HSM gerenciado chamado testmhsm e salva um backup dessa chave em um arquivo que é automaticamente nomeado para você e exibe o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="11630-118">This command retrieves the key named testkey from the managed HSM named testmhsm and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

## <span data-ttu-id="11630-119">OS</span><span class="sxs-lookup"><span data-stu-id="11630-119">PARAMETERS</span></span>

### <span data-ttu-id="11630-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11630-120">-DefaultProfile</span></span>
<span data-ttu-id="11630-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="11630-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11630-122">-Force</span><span class="sxs-lookup"><span data-stu-id="11630-122">-Force</span></span>
<span data-ttu-id="11630-123">Substituir o arquivo fornecido se ele existir</span><span class="sxs-lookup"><span data-stu-id="11630-123">Overwrite the given file if it exists</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11630-124">-HsmName</span><span class="sxs-lookup"><span data-stu-id="11630-124">-HsmName</span></span>
<span data-ttu-id="11630-125">Nome do HSM.</span><span class="sxs-lookup"><span data-stu-id="11630-125">HSM name.</span></span> <span data-ttu-id="11630-126">O cmdlet constrói o FQDN de um HSM gerenciado com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="11630-126">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11630-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11630-127">-InputObject</span></span>
<span data-ttu-id="11630-128">Pacote de chaves para backup, em pipeline a partir da saída de uma chamada de recuperação.</span><span class="sxs-lookup"><span data-stu-id="11630-128">Key bundle to back up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByKey
Aliases: Key

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11630-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="11630-129">-Name</span></span>
<span data-ttu-id="11630-130">Nome da chave.</span><span class="sxs-lookup"><span data-stu-id="11630-130">Key name.</span></span>
<span data-ttu-id="11630-131">O cmdlet constrói o FQDN de uma chave do nome gerenciado do HSM, o ambiente selecionado no momento e o nome da chave.</span><span class="sxs-lookup"><span data-stu-id="11630-131">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11630-132">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="11630-132">-OutputFile</span></span>
<span data-ttu-id="11630-133">Arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="11630-133">Output file.</span></span>
<span data-ttu-id="11630-134">O arquivo de saída para armazenar o blob de chave de backup em.</span><span class="sxs-lookup"><span data-stu-id="11630-134">The output file to store the backed up key blob in.</span></span>
<span data-ttu-id="11630-135">Se não estiver presente, um nome de arquivo padrão será escolhido.</span><span class="sxs-lookup"><span data-stu-id="11630-135">If not present, a default filename is chosen.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11630-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="11630-136">-Confirm</span></span>
<span data-ttu-id="11630-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11630-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11630-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11630-138">-WhatIf</span></span>
<span data-ttu-id="11630-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="11630-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11630-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="11630-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11630-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11630-141">CommonParameters</span></span>
<span data-ttu-id="11630-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11630-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11630-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11630-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11630-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="11630-144">INPUTS</span></span>

### <span data-ttu-id="11630-145">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="11630-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="11630-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="11630-146">OUTPUTS</span></span>

### <span data-ttu-id="11630-147">System. String</span><span class="sxs-lookup"><span data-stu-id="11630-147">System.String</span></span>

## <span data-ttu-id="11630-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="11630-148">NOTES</span></span>

## <span data-ttu-id="11630-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11630-149">RELATED LINKS</span></span>

[<span data-ttu-id="11630-150">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="11630-150">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="11630-151">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="11630-151">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="11630-152">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="11630-152">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="11630-153">Desfazer-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="11630-153">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="11630-154">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="11630-154">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="11630-155">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="11630-155">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)