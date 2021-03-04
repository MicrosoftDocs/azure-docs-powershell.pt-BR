---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/undo-azkeyvaultcertificateremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
ms.openlocfilehash: e514ded413eaca5ae5992e452a6b35f78ab6532b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890391"
---
# <span data-ttu-id="d8e4a-101">Undo-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="d8e4a-101">Undo-AzKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="d8e4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8e4a-102">SYNOPSIS</span></span>
<span data-ttu-id="d8e4a-103">Recupera um certificado excluído em um cofre de chaves em um estado ativo.</span><span class="sxs-lookup"><span data-stu-id="d8e4a-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

## <span data-ttu-id="d8e4a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d8e4a-104">SYNTAX</span></span>

### <span data-ttu-id="d8e4a-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d8e4a-105">Default (Default)</span></span>
```
Undo-AzKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8e4a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d8e4a-106">InputObject</span></span>
```
Undo-AzKeyVaultCertificateRemoval [-InputObject] <PSDeletedKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8e4a-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d8e4a-107">DESCRIPTION</span></span>
<span data-ttu-id="d8e4a-108">O cmdlet **Undo-AzKeyVaultCertificateRemoval** recuperará um certificado excluído anteriormente.</span><span class="sxs-lookup"><span data-stu-id="d8e4a-108">The **Undo-AzKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="d8e4a-109">O certificado recuperado estará ativo e poderá ser usado para todas as operações.</span><span class="sxs-lookup"><span data-stu-id="d8e4a-109">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="d8e4a-110">O chamador precisa ter permissão de 'recuperar' para executar essa operação.</span><span class="sxs-lookup"><span data-stu-id="d8e4a-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="d8e4a-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d8e4a-111">EXAMPLES</span></span>

### <span data-ttu-id="d8e4a-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d8e4a-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'

Certificate   : [Subject]
                  CN=contoso.com

                [Issuer]
                  CN=contoso.com

                [Serial Number]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                [Not Before]
                  5/24/2018 10:58:13 AM

                [Not After]
                  11/24/2018 10:08:13 AM

                [Thumbprint]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId         : https://mykeyvault.vault.azure.net:443/keys/mycertificate/7fe415d5518240c1a6fce89986b8d334
SecretId      : https://mykeyvault.vault.azure.net:443/secrets/mycertificate/7fe415d5518240c1a6fce89986b8d334
Thumbprint    : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel : Recoverable+Purgeable
Enabled       : True
Expires       : 11/24/2018 6:08:13 PM
NotBefore     : 5/24/2018 5:58:13 PM
Created       : 5/24/2018 6:08:13 PM
Updated       : 5/24/2018 6:08:13 PM
Tags          :
VaultName     : MyKeyVault
Name          : MyCertificate
Version       : 7fe415d5518240c1a6fce89986b8d334
Id            : https://mykeyvault.vault.azure.net:443/certificates/mycertificate/7fe415d5518240c1a6fce89986b8d334
```

<span data-ttu-id="d8e4a-113">Este comando recuperará o certificado 'MyCertificate' que foi excluído anteriormente, em um estado ativo e acessível.</span><span class="sxs-lookup"><span data-stu-id="d8e4a-113">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="d8e4a-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d8e4a-114">PARAMETERS</span></span>

### <span data-ttu-id="d8e4a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8e4a-115">-DefaultProfile</span></span>
<span data-ttu-id="d8e4a-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="d8e4a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8e4a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8e4a-117">-InputObject</span></span>
<span data-ttu-id="d8e4a-118">Objeto Certificate excluído</span><span class="sxs-lookup"><span data-stu-id="d8e4a-118">Deleted Certificate object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8e4a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d8e4a-119">-Name</span></span>
<span data-ttu-id="d8e4a-120">Nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="d8e4a-120">Certificate name.</span></span>
<span data-ttu-id="d8e4a-121">O cmdlet constrói o FQDN de um certificado a partir do nome do cofre, do ambiente selecionado no momento e do nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="d8e4a-121">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8e4a-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d8e4a-122">-VaultName</span></span>
<span data-ttu-id="d8e4a-123">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="d8e4a-123">Vault name.</span></span>
<span data-ttu-id="d8e4a-124">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="d8e4a-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8e4a-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8e4a-125">-Confirm</span></span>
<span data-ttu-id="d8e4a-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8e4a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8e4a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8e4a-127">-WhatIf</span></span>
<span data-ttu-id="d8e4a-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d8e4a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8e4a-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d8e4a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8e4a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8e4a-130">CommonParameters</span></span>
<span data-ttu-id="d8e4a-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8e4a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8e4a-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8e4a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8e4a-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d8e4a-133">INPUTS</span></span>

### <span data-ttu-id="d8e4a-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="d8e4a-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="d8e4a-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d8e4a-135">OUTPUTS</span></span>

### <span data-ttu-id="d8e4a-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d8e4a-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="d8e4a-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="d8e4a-137">NOTES</span></span>

## <span data-ttu-id="d8e4a-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d8e4a-138">RELATED LINKS</span></span>

[<span data-ttu-id="d8e4a-139">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d8e4a-139">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="d8e4a-140">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d8e4a-140">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)
