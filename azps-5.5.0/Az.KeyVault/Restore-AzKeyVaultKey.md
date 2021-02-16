---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
ms.openlocfilehash: 958aeb36ba047284085d471f73aadad78b756839
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113100"
---
# <span data-ttu-id="aec05-101">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="aec05-101">Restore-AzKeyVaultKey</span></span>

## <span data-ttu-id="aec05-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aec05-102">SYNOPSIS</span></span>
<span data-ttu-id="aec05-103">Cria uma chave em um cofre de chave a partir de uma chave em backup.</span><span class="sxs-lookup"><span data-stu-id="aec05-103">Creates a key in a key vault from a backed-up key.</span></span>

## <span data-ttu-id="aec05-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aec05-104">SYNTAX</span></span>

### <span data-ttu-id="aec05-105">ByVaultName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="aec05-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aec05-106">HsmByVaultName</span><span class="sxs-lookup"><span data-stu-id="aec05-106">HsmByVaultName</span></span>
```
Restore-AzKeyVaultKey -HsmName <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aec05-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="aec05-107">ByInputObject</span></span>
```
Restore-AzKeyVaultKey [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aec05-108">HsmByInputObject</span><span class="sxs-lookup"><span data-stu-id="aec05-108">HsmByInputObject</span></span>
```
Restore-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aec05-109">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="aec05-109">ByResourceId</span></span>
```
Restore-AzKeyVaultKey [-ResourceId] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aec05-110">HsmByResourceId</span><span class="sxs-lookup"><span data-stu-id="aec05-110">HsmByResourceId</span></span>
```
Restore-AzKeyVaultKey -HsmResourceId <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aec05-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="aec05-111">DESCRIPTION</span></span>
<span data-ttu-id="aec05-112">O **cmdlet Restore-AzKeyVaultKey** cria uma chave no cofre de chave especificado.</span><span class="sxs-lookup"><span data-stu-id="aec05-112">The **Restore-AzKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="aec05-113">Essa chave é uma réplica da tecla em backup no arquivo de entrada e tem o mesmo nome da chave original.</span><span class="sxs-lookup"><span data-stu-id="aec05-113">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="aec05-114">Se o cofre de teclas já tiver uma chave com o mesmo nome, esse cmdlet falhará em vez de sobrescrever a chave original.</span><span class="sxs-lookup"><span data-stu-id="aec05-114">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="aec05-115">Se o backup contiver várias versões de uma chave, todas as versões serão restauradas.</span><span class="sxs-lookup"><span data-stu-id="aec05-115">If the backup contains multiple versions of a key, all versions are restored.</span></span>
<span data-ttu-id="aec05-116">O cofre de chave no que você restaurar a chave pode ser diferente do cofre de chave do onde você fez backup da chave.</span><span class="sxs-lookup"><span data-stu-id="aec05-116">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="aec05-117">No entanto, o cofre de chave deve usar a mesma assinatura e estar em uma região do Azure na mesma geografia (por exemplo, América do Norte).</span><span class="sxs-lookup"><span data-stu-id="aec05-117">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="aec05-118">Consulte a Central de Confiadura do Microsoft Azure ( para o mapeamento de regiões https://azure.microsoft.com/support/trust-center/) do Azure para regiões geográficas.</span><span class="sxs-lookup"><span data-stu-id="aec05-118">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="aec05-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="aec05-119">EXAMPLES</span></span>

### <span data-ttu-id="aec05-120">Exemplo 1: Restaurar uma chave de backup</span><span class="sxs-lookup"><span data-stu-id="aec05-120">Example 1: Restore a backed-up key</span></span>
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

<span data-ttu-id="aec05-121">Esse comando restaura uma chave, incluindo todas as suas versões, do arquivo de backup chamado Backup.blob para o cofre de chave chamado MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="aec05-121">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="aec05-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aec05-122">PARAMETERS</span></span>

### <span data-ttu-id="aec05-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aec05-123">-DefaultProfile</span></span>
<span data-ttu-id="aec05-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="aec05-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aec05-125">-HsmName</span><span class="sxs-lookup"><span data-stu-id="aec05-125">-HsmName</span></span>
<span data-ttu-id="aec05-126">Nome HSM.</span><span class="sxs-lookup"><span data-stu-id="aec05-126">HSM name.</span></span> <span data-ttu-id="aec05-127">O Cmdlet construirá o FQDN de um HSM gerenciado com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="aec05-127">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aec05-128">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="aec05-128">-HsmObject</span></span>
<span data-ttu-id="aec05-129">Objeto HSM</span><span class="sxs-lookup"><span data-stu-id="aec05-129">HSM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: HsmByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aec05-130">-HsmResourceId</span><span class="sxs-lookup"><span data-stu-id="aec05-130">-HsmResourceId</span></span>
<span data-ttu-id="aec05-131">ID do Recurso Hsm</span><span class="sxs-lookup"><span data-stu-id="aec05-131">Hsm Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aec05-132">-InputFile</span><span class="sxs-lookup"><span data-stu-id="aec05-132">-InputFile</span></span>
<span data-ttu-id="aec05-133">Especifica o arquivo de entrada que contém o backup da chave a ser restaurada.</span><span class="sxs-lookup"><span data-stu-id="aec05-133">Specifies the input file that contains the backup of the key to restore.</span></span>

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

### <span data-ttu-id="aec05-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aec05-134">-InputObject</span></span>
<span data-ttu-id="aec05-135">Objeto KeyVault</span><span class="sxs-lookup"><span data-stu-id="aec05-135">KeyVault object</span></span>

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

### <span data-ttu-id="aec05-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aec05-136">-ResourceId</span></span>
<span data-ttu-id="aec05-137">ID do Recurso KeyVault</span><span class="sxs-lookup"><span data-stu-id="aec05-137">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="aec05-138">-Nomedo Cofre</span><span class="sxs-lookup"><span data-stu-id="aec05-138">-VaultName</span></span>
<span data-ttu-id="aec05-139">Especifica o nome do cofre de chave para restaurar a chave.</span><span class="sxs-lookup"><span data-stu-id="aec05-139">Specifies the name of the key vault into which to restore the key.</span></span>

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

### <span data-ttu-id="aec05-140">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="aec05-140">-Confirm</span></span>
<span data-ttu-id="aec05-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aec05-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aec05-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aec05-142">-WhatIf</span></span>
<span data-ttu-id="aec05-143">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="aec05-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aec05-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aec05-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aec05-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aec05-145">CommonParameters</span></span>
<span data-ttu-id="aec05-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aec05-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aec05-147">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aec05-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aec05-148">Entradas</span><span class="sxs-lookup"><span data-stu-id="aec05-148">INPUTS</span></span>

### <span data-ttu-id="aec05-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="aec05-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="aec05-150">System.String</span><span class="sxs-lookup"><span data-stu-id="aec05-150">System.String</span></span>

## <span data-ttu-id="aec05-151">Saídas</span><span class="sxs-lookup"><span data-stu-id="aec05-151">OUTPUTS</span></span>

### <span data-ttu-id="aec05-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="aec05-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="aec05-153">Notas</span><span class="sxs-lookup"><span data-stu-id="aec05-153">NOTES</span></span>

## <span data-ttu-id="aec05-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aec05-154">RELATED LINKS</span></span>

[<span data-ttu-id="aec05-155">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="aec05-155">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="aec05-156">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="aec05-156">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="aec05-157">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="aec05-157">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="aec05-158">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="aec05-158">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

