---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/import-azkeyvaultsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultSecurityDomain.md
ms.openlocfilehash: f96aa323486144ec9d4dcb04ff00f408a763a81a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262864"
---
# <span data-ttu-id="9979e-101">Import-AzKeyVaultSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="9979e-101">Import-AzKeyVaultSecurityDomain</span></span>

## <span data-ttu-id="9979e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9979e-102">SYNOPSIS</span></span>
<span data-ttu-id="9979e-103">Importa dados de domínio de segurança exportados anteriormente para um HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="9979e-103">Imports previously exported security domain data to a managed HSM.</span></span>

## <span data-ttu-id="9979e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9979e-104">SYNTAX</span></span>

### <span data-ttu-id="9979e-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="9979e-105">ByName (Default)</span></span>
```
Import-AzKeyVaultSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9979e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9979e-106">ByInputObject</span></span>
```
Import-AzKeyVaultSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru]
 -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9979e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9979e-107">DESCRIPTION</span></span>
<span data-ttu-id="9979e-108">Este cmdlet importa dados de domínio de segurança exportados anteriormente para um HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="9979e-108">This cmdlet imports previously exported security domain data to a managed HSM.</span></span>

## <span data-ttu-id="9979e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9979e-109">EXAMPLES</span></span>

### <span data-ttu-id="9979e-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9979e-110">Example 1</span></span>
```powershell
PS C:\> $keys = @{PublicKey = "sd1.cer"; PrivateKey = "sd1.key"}, @{PublicKey = "sd2.cer"; PrivateKey = "sd2.key"}, @{PublicKey = "sd3.cer"; PrivateKey = "sd3.key"}
PS C:\> Import-AzKeyVaultSecurityDomain -Name testmhsm -Keys $keys -SecurityDomainPath {pathOfBackup}\sd.ps.json
```

<span data-ttu-id="9979e-111">Primeiro, as chaves precisam ser fornecidas para descriptografar os dados do domínio de segurança.</span><span class="sxs-lookup"><span data-stu-id="9979e-111">First, the keys need be provided to decrypt the security domain data.</span></span>
<span data-ttu-id="9979e-112">Em seguida, o comando **Import-AzKeyVaultSecurityDomain** restaura dados do domínio de segurança anteriores para um HSM gerenciado usando essas chaves.</span><span class="sxs-lookup"><span data-stu-id="9979e-112">Then, The **Import-AzKeyVaultSecurityDomain** command restores previous backed up security domain data to a managed HSM using these keys.</span></span>

## <span data-ttu-id="9979e-113">OS</span><span class="sxs-lookup"><span data-stu-id="9979e-113">PARAMETERS</span></span>

### <span data-ttu-id="9979e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9979e-114">-DefaultProfile</span></span>
<span data-ttu-id="9979e-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9979e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9979e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9979e-116">-InputObject</span></span>
<span data-ttu-id="9979e-117">Objeto que representa um HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="9979e-117">Object representing a managed HSM.</span></span>

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

### <span data-ttu-id="9979e-118">-Teclas</span><span class="sxs-lookup"><span data-stu-id="9979e-118">-Keys</span></span>
<span data-ttu-id="9979e-119">Informações sobre as chaves usadas para descriptografar os dados do domínio de segurança.</span><span class="sxs-lookup"><span data-stu-id="9979e-119">Information about the keys that are used to decrypt the security domain data.</span></span>
<span data-ttu-id="9979e-120">Veja exemplos de como ele é construído.</span><span class="sxs-lookup"><span data-stu-id="9979e-120">See examples for how it is constructed.</span></span>

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

### <span data-ttu-id="9979e-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="9979e-121">-Name</span></span>
<span data-ttu-id="9979e-122">Nome do HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="9979e-122">Name of the managed HSM.</span></span>

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

### <span data-ttu-id="9979e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9979e-123">-PassThru</span></span>
<span data-ttu-id="9979e-124">Quando especificado, um booliano será retornado quando o cmdlet for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="9979e-124">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="9979e-125">-SecurityDomainPath</span><span class="sxs-lookup"><span data-stu-id="9979e-125">-SecurityDomainPath</span></span>
<span data-ttu-id="9979e-126">Especifique o caminho para os dados do domínio de segurança criptografados.</span><span class="sxs-lookup"><span data-stu-id="9979e-126">Specify the path to the encrypted security domain data.</span></span>

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

### <span data-ttu-id="9979e-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9979e-127">-Confirm</span></span>
<span data-ttu-id="9979e-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9979e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9979e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9979e-129">-WhatIf</span></span>
<span data-ttu-id="9979e-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9979e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9979e-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9979e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9979e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9979e-132">CommonParameters</span></span>
<span data-ttu-id="9979e-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9979e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9979e-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9979e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9979e-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9979e-135">INPUTS</span></span>

### <span data-ttu-id="9979e-136">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="9979e-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="9979e-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9979e-137">OUTPUTS</span></span>

### <span data-ttu-id="9979e-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9979e-138">System.Boolean</span></span>

## <span data-ttu-id="9979e-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9979e-139">NOTES</span></span>

## <span data-ttu-id="9979e-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9979e-140">RELATED LINKS</span></span>
