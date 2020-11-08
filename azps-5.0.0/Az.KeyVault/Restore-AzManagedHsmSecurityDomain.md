---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azmanagedhsmsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsmSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsmSecurityDomain.md
ms.openlocfilehash: f743b408917e575005589598a49fafbd8cc95379
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94126137"
---
# <span data-ttu-id="cefda-101">Restore-AzManagedHsmSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="cefda-101">Restore-AzManagedHsmSecurityDomain</span></span>

## <span data-ttu-id="cefda-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cefda-102">SYNOPSIS</span></span>
<span data-ttu-id="cefda-103">Restaura dados do domínio de segurança anteriores em backup para um HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="cefda-103">Restores previous backed up security domain data to a managed HSM.</span></span>

## <span data-ttu-id="cefda-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cefda-104">SYNTAX</span></span>

### <span data-ttu-id="cefda-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="cefda-105">ByName (Default)</span></span>
```
Restore-AzManagedHsmSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cefda-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cefda-106">ByInputObject</span></span>
```
Restore-AzManagedHsmSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru]
 -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cefda-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cefda-107">DESCRIPTION</span></span>
<span data-ttu-id="cefda-108">Este cmdlet restaura dados do domínio de segurança anteriores em backup para um HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="cefda-108">This cmdlet restores previous backed up security domain data to a managed HSM.</span></span>

## <span data-ttu-id="cefda-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cefda-109">EXAMPLES</span></span>

### <span data-ttu-id="cefda-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cefda-110">Example 1</span></span>
```powershell
PS C:\> $keys = @{PublicKey = "sd1.cer"; PrivateKey = "sd1.key"}, @{PublicKey = "sd2.cer"; PrivateKey = "sd2.key"}, @{PublicKey = "sd3.cer"; PrivateKey = "sd3.key"}
PS C:\> Restore-AzManagedHsmSecurityDomain -Name testmhsm -Keys $keys -SecurityDomainPath {pathOfBackup}\sd.ps.json
```

<span data-ttu-id="cefda-111">Primeiro, as chaves precisam ser fornecidas para descriptografar os dados do domínio de segurança.</span><span class="sxs-lookup"><span data-stu-id="cefda-111">First, the keys need be provided to decrypt the security domain data.</span></span> <span data-ttu-id="cefda-112">Em seguida, o comando **Restore-AzManagedHsmSecurityDomain** restaura os dados do domínio de segurança do backup anterior para um HSM gerenciado usando essas chaves.</span><span class="sxs-lookup"><span data-stu-id="cefda-112">Then, The **Restore-AzManagedHsmSecurityDomain** command restores previous backed up security domain data to a managed HSM using these keys.</span></span>

## <span data-ttu-id="cefda-113">OS</span><span class="sxs-lookup"><span data-stu-id="cefda-113">PARAMETERS</span></span>

### <span data-ttu-id="cefda-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cefda-114">-DefaultProfile</span></span>
<span data-ttu-id="cefda-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cefda-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cefda-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cefda-116">-InputObject</span></span>
<span data-ttu-id="cefda-117">Objeto que representa um HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="cefda-117">Object representing a managed HSM.</span></span>

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

### <span data-ttu-id="cefda-118">-Teclas</span><span class="sxs-lookup"><span data-stu-id="cefda-118">-Keys</span></span>
<span data-ttu-id="cefda-119">Informações sobre as chaves usadas para descriptografar os dados do domínio de segurança.</span><span class="sxs-lookup"><span data-stu-id="cefda-119">Information about the keys that are used to decrypt the security domain data.</span></span>
<span data-ttu-id="cefda-120">Veja exemplos de como ele é construído.</span><span class="sxs-lookup"><span data-stu-id="cefda-120">See examples for how it is constructed.</span></span>

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

### <span data-ttu-id="cefda-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="cefda-121">-Name</span></span>
<span data-ttu-id="cefda-122">Nome do HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="cefda-122">Name of the managed HSM.</span></span>

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

### <span data-ttu-id="cefda-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cefda-123">-PassThru</span></span>
<span data-ttu-id="cefda-124">Quando especificado, um booliano será retornado quando o cmdlet for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="cefda-124">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="cefda-125">-SecurityDomainPath</span><span class="sxs-lookup"><span data-stu-id="cefda-125">-SecurityDomainPath</span></span>
<span data-ttu-id="cefda-126">Especifique o caminho para os dados do domínio de segurança criptografados.</span><span class="sxs-lookup"><span data-stu-id="cefda-126">Specify the path to the encrypted security domain data.</span></span>

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

### <span data-ttu-id="cefda-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cefda-127">-Confirm</span></span>
<span data-ttu-id="cefda-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cefda-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cefda-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cefda-129">-WhatIf</span></span>
<span data-ttu-id="cefda-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cefda-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cefda-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cefda-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cefda-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cefda-132">CommonParameters</span></span>
<span data-ttu-id="cefda-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cefda-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cefda-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cefda-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cefda-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cefda-135">INPUTS</span></span>

### <span data-ttu-id="cefda-136">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="cefda-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="cefda-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cefda-137">OUTPUTS</span></span>

### <span data-ttu-id="cefda-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cefda-138">System.Boolean</span></span>

## <span data-ttu-id="cefda-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cefda-139">NOTES</span></span>

## <span data-ttu-id="cefda-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cefda-140">RELATED LINKS</span></span>
