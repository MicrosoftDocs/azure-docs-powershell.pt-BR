---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsmKey.md
ms.openlocfilehash: 38e0dbf124643a7d669c1787314790166e88f6a9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94126143"
---
# <span data-ttu-id="ecc41-101">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="ecc41-101">Restore-AzManagedHsmKey</span></span>

## <span data-ttu-id="ecc41-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ecc41-102">SYNOPSIS</span></span>
<span data-ttu-id="ecc41-103">Cria uma chave em um HSM gerenciado a partir de uma chave com backup.</span><span class="sxs-lookup"><span data-stu-id="ecc41-103">Creates a key in a managed HSM from a backed-up key.</span></span>

## <span data-ttu-id="ecc41-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ecc41-104">SYNTAX</span></span>

### <span data-ttu-id="ecc41-105">ByHsmName (padrão)</span><span class="sxs-lookup"><span data-stu-id="ecc41-105">ByHsmName (Default)</span></span>
```
Restore-AzManagedHsmKey [-HsmName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecc41-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ecc41-106">ByInputObject</span></span>
```
Restore-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecc41-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ecc41-107">ByResourceId</span></span>
```
Restore-AzManagedHsmKey [-ResourceId] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecc41-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ecc41-108">DESCRIPTION</span></span>
<span data-ttu-id="ecc41-109">O cmdlet **Restore-AzManagedHsmKey** cria uma chave no HSM gerenciado especificado.</span><span class="sxs-lookup"><span data-stu-id="ecc41-109">The **Restore-AzManagedHsmKey** cmdlet creates a key in the specified managed HSM.</span></span>
<span data-ttu-id="ecc41-110">Essa chave é uma réplica da chave com backup no arquivo de entrada e tem o mesmo nome da chave original.</span><span class="sxs-lookup"><span data-stu-id="ecc41-110">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="ecc41-111">Se o HSM gerenciado já tem uma chave com o mesmo nome, esse cmdlet falha em vez de substituir a chave original.</span><span class="sxs-lookup"><span data-stu-id="ecc41-111">If the managed HSM already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="ecc41-112">Se o backup contiver várias versões de uma chave, todas as versões serão restauradas.</span><span class="sxs-lookup"><span data-stu-id="ecc41-112">If the backup contains multiple versions of a key, all versions are restored.</span></span>
<span data-ttu-id="ecc41-113">O HSM gerenciado para o qual você restaura a chave pode ser diferente do HSM gerenciado do qual você tem o backup da chave.</span><span class="sxs-lookup"><span data-stu-id="ecc41-113">The managed HSM that you restore the key into can be different from the managed HSM that you backed up the key from.</span></span>
<span data-ttu-id="ecc41-114">No entanto, o HSM gerenciado deve usar a mesma assinatura e estar em uma região do Azure na mesma Geografia (por exemplo, América do Norte).</span><span class="sxs-lookup"><span data-stu-id="ecc41-114">However, the managed HSM must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="ecc41-115">Consulte a central de confiabilidade do Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) para o mapeamento de regiões do Azure para regiões geográficas.</span><span class="sxs-lookup"><span data-stu-id="ecc41-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="ecc41-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ecc41-116">EXAMPLES</span></span>

### <span data-ttu-id="ecc41-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ecc41-117">Example 1</span></span>
```powershell
PS C:\> Restore-AzManagedHsmKey -HsmName testmhsm -InputFile "C:\Backup.blob"

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 7cff8510da04433b98144a3e33ad2bae
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/7cff8510da04433b98144a3e33ad2bae
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 10:13:03 AM
Updated        : 10/14/2020 10:13:03 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="ecc41-118">Esse comando restaura uma chave, incluindo todas as suas versões, do arquivo de backup chamado backup. blob no HSM gerenciado chamado testmhsm.</span><span class="sxs-lookup"><span data-stu-id="ecc41-118">This command restores a key, including all of its versions, from the backup file named Backup.blob into the managed HSM named testmhsm.</span></span>

## <span data-ttu-id="ecc41-119">OS</span><span class="sxs-lookup"><span data-stu-id="ecc41-119">PARAMETERS</span></span>

### <span data-ttu-id="ecc41-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecc41-120">-DefaultProfile</span></span>
<span data-ttu-id="ecc41-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ecc41-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecc41-122">-HsmName</span><span class="sxs-lookup"><span data-stu-id="ecc41-122">-HsmName</span></span>
<span data-ttu-id="ecc41-123">Nome do HSM.</span><span class="sxs-lookup"><span data-stu-id="ecc41-123">HSM name.</span></span> <span data-ttu-id="ecc41-124">O cmdlet constrói o FQDN de um HSM gerenciado com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="ecc41-124">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHsmName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecc41-125">-InputFile</span><span class="sxs-lookup"><span data-stu-id="ecc41-125">-InputFile</span></span>
<span data-ttu-id="ecc41-126">Arquivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="ecc41-126">Input file.</span></span>
<span data-ttu-id="ecc41-127">O arquivo de entrada que contém o blob com backup</span><span class="sxs-lookup"><span data-stu-id="ecc41-127">The input file containing the backed-up blob</span></span>

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

### <span data-ttu-id="ecc41-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ecc41-128">-InputObject</span></span>
<span data-ttu-id="ecc41-129">Objeto HSM</span><span class="sxs-lookup"><span data-stu-id="ecc41-129">HSM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ecc41-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ecc41-130">-ResourceId</span></span>
<span data-ttu-id="ecc41-131">ID do recurso HSM</span><span class="sxs-lookup"><span data-stu-id="ecc41-131">HSM Resource Id</span></span>

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

### <span data-ttu-id="ecc41-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ecc41-132">-Confirm</span></span>
<span data-ttu-id="ecc41-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecc41-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecc41-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecc41-134">-WhatIf</span></span>
<span data-ttu-id="ecc41-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ecc41-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecc41-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ecc41-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecc41-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecc41-137">CommonParameters</span></span>
<span data-ttu-id="ecc41-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecc41-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecc41-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ecc41-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecc41-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ecc41-140">INPUTS</span></span>

### <span data-ttu-id="ecc41-141">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="ecc41-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="ecc41-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ecc41-142">System.String</span></span>

## <span data-ttu-id="ecc41-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ecc41-143">OUTPUTS</span></span>

### <span data-ttu-id="ecc41-144">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ecc41-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="ecc41-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ecc41-145">NOTES</span></span>

## <span data-ttu-id="ecc41-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ecc41-146">RELATED LINKS</span></span>

[<span data-ttu-id="ecc41-147">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="ecc41-147">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="ecc41-148">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="ecc41-148">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="ecc41-149">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="ecc41-149">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="ecc41-150">Desfazer-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="ecc41-150">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="ecc41-151">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="ecc41-151">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="ecc41-152">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="ecc41-152">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)