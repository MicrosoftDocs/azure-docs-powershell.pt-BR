---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/import-azkeyvaultsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultSecurityDomain.md
ms.openlocfilehash: f96aa323486144ec9d4dcb04ff00f408a763a81a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118960"
---
# <span data-ttu-id="c4bf5-101">Import-AzKeyVaultSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="c4bf5-101">Import-AzKeyVaultSecurityDomain</span></span>

## <span data-ttu-id="c4bf5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c4bf5-102">SYNOPSIS</span></span>
<span data-ttu-id="c4bf5-103">Importa dados de domínio de segurança exportados anteriormente para um HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="c4bf5-103">Imports previously exported security domain data to a managed HSM.</span></span>

## <span data-ttu-id="c4bf5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c4bf5-104">SYNTAX</span></span>

### <span data-ttu-id="c4bf5-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="c4bf5-105">ByName (Default)</span></span>
```
Import-AzKeyVaultSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4bf5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c4bf5-106">ByInputObject</span></span>
```
Import-AzKeyVaultSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru]
 -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c4bf5-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="c4bf5-107">DESCRIPTION</span></span>
<span data-ttu-id="c4bf5-108">Este cmdlet importa dados de domínio de segurança exportados anteriormente para um HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="c4bf5-108">This cmdlet imports previously exported security domain data to a managed HSM.</span></span>

## <span data-ttu-id="c4bf5-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c4bf5-109">EXAMPLES</span></span>

### <span data-ttu-id="c4bf5-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c4bf5-110">Example 1</span></span>
```powershell
PS C:\> $keys = @{PublicKey = "sd1.cer"; PrivateKey = "sd1.key"}, @{PublicKey = "sd2.cer"; PrivateKey = "sd2.key"}, @{PublicKey = "sd3.cer"; PrivateKey = "sd3.key"}
PS C:\> Import-AzKeyVaultSecurityDomain -Name testmhsm -Keys $keys -SecurityDomainPath {pathOfBackup}\sd.ps.json
```

<span data-ttu-id="c4bf5-111">Primeiro, as chaves precisam ser fornecidas para descriptografar os dados do domínio de segurança.</span><span class="sxs-lookup"><span data-stu-id="c4bf5-111">First, the keys need be provided to decrypt the security domain data.</span></span>
<span data-ttu-id="c4bf5-112">Em seguida, **o comando Import-AzKeyVaultSecurityDomain** restaura dados de domínio de segurança de backup anteriores para um HSM gerenciado usando essas chaves.</span><span class="sxs-lookup"><span data-stu-id="c4bf5-112">Then, The **Import-AzKeyVaultSecurityDomain** command restores previous backed up security domain data to a managed HSM using these keys.</span></span>

## <span data-ttu-id="c4bf5-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c4bf5-113">PARAMETERS</span></span>

### <span data-ttu-id="c4bf5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4bf5-114">-DefaultProfile</span></span>
<span data-ttu-id="c4bf5-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c4bf5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4bf5-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4bf5-116">-InputObject</span></span>
<span data-ttu-id="c4bf5-117">Objeto que representa um HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="c4bf5-117">Object representing a managed HSM.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4bf5-118">-Teclas</span><span class="sxs-lookup"><span data-stu-id="c4bf5-118">-Keys</span></span>
<span data-ttu-id="c4bf5-119">Informações sobre as chaves usadas para descriptografar os dados do domínio de segurança.</span><span class="sxs-lookup"><span data-stu-id="c4bf5-119">Information about the keys that are used to decrypt the security domain data.</span></span>
<span data-ttu-id="c4bf5-120">Veja exemplos de como ele é construído.</span><span class="sxs-lookup"><span data-stu-id="c4bf5-120">See examples for how it is constructed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.SecurityDomain.Models.KeyPath[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4bf5-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="c4bf5-121">-Name</span></span>
<span data-ttu-id="c4bf5-122">Nome do HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="c4bf5-122">Name of the managed HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: HsmName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4bf5-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4bf5-123">-PassThru</span></span>
<span data-ttu-id="c4bf5-124">Quando especificado, um boolano será retornado quando o cmdlet for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="c4bf5-124">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="c4bf5-125">-SecurityDomainPath</span><span class="sxs-lookup"><span data-stu-id="c4bf5-125">-SecurityDomainPath</span></span>
<span data-ttu-id="c4bf5-126">Especifique o caminho para os dados de domínio de segurança criptografados.</span><span class="sxs-lookup"><span data-stu-id="c4bf5-126">Specify the path to the encrypted security domain data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4bf5-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c4bf5-127">-Confirm</span></span>
<span data-ttu-id="c4bf5-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4bf5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4bf5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4bf5-129">-WhatIf</span></span>
<span data-ttu-id="c4bf5-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c4bf5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4bf5-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c4bf5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4bf5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4bf5-132">CommonParameters</span></span>
<span data-ttu-id="c4bf5-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4bf5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4bf5-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c4bf5-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4bf5-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="c4bf5-135">INPUTS</span></span>

### <span data-ttu-id="c4bf5-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="c4bf5-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="c4bf5-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="c4bf5-137">OUTPUTS</span></span>

### <span data-ttu-id="c4bf5-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c4bf5-138">System.Boolean</span></span>

## <span data-ttu-id="c4bf5-139">Notas</span><span class="sxs-lookup"><span data-stu-id="c4bf5-139">NOTES</span></span>

## <span data-ttu-id="c4bf5-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c4bf5-140">RELATED LINKS</span></span>
