---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultcertificateremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
ms.openlocfilehash: db2b9066524bd21daa1fa65b87554d9b028754de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440787"
---
# <span data-ttu-id="93bdf-101">Undo-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="93bdf-101">Undo-AzureKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="93bdf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="93bdf-102">SYNOPSIS</span></span>
<span data-ttu-id="93bdf-103">Recupera um certificado excluído em um cofre de chaves para um estado ativo.</span><span class="sxs-lookup"><span data-stu-id="93bdf-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93bdf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="93bdf-104">SYNTAX</span></span>

### <span data-ttu-id="93bdf-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="93bdf-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93bdf-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="93bdf-106">InputObject</span></span>
```
Undo-AzureKeyVaultCertificateRemoval [-InputObject] <PSDeletedKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93bdf-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="93bdf-107">DESCRIPTION</span></span>
<span data-ttu-id="93bdf-108">O cmdlet **Undo-AzureKeyVaultCertificateRemoval** irá recuperar um certificado excluído anteriormente.</span><span class="sxs-lookup"><span data-stu-id="93bdf-108">The **Undo-AzureKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="93bdf-109">O certificado recuperado estará ativo e poderá ser usado para todas as operações.</span><span class="sxs-lookup"><span data-stu-id="93bdf-109">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="93bdf-110">O chamador precisa ter a permissão ' recuperar ' para executar essa operação.</span><span class="sxs-lookup"><span data-stu-id="93bdf-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="93bdf-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="93bdf-111">EXAMPLES</span></span>

### <span data-ttu-id="93bdf-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="93bdf-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzureKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'

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

<span data-ttu-id="93bdf-113">Esse comando recuperará o certificado ' myCertificate ' que foi excluído anteriormente em um estado ativo e utilizável.</span><span class="sxs-lookup"><span data-stu-id="93bdf-113">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="93bdf-114">OS</span><span class="sxs-lookup"><span data-stu-id="93bdf-114">PARAMETERS</span></span>

### <span data-ttu-id="93bdf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93bdf-115">-DefaultProfile</span></span>
<span data-ttu-id="93bdf-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="93bdf-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93bdf-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93bdf-117">-InputObject</span></span>
<span data-ttu-id="93bdf-118">Objeto de certificado excluído</span><span class="sxs-lookup"><span data-stu-id="93bdf-118">Deleted Certificate object</span></span>

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

### <span data-ttu-id="93bdf-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="93bdf-119">-Name</span></span>
<span data-ttu-id="93bdf-120">Nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="93bdf-120">Certificate name.</span></span>
<span data-ttu-id="93bdf-121">O cmdlet constrói o FQDN de um certificado a partir do nome do cofre, do ambiente selecionado no momento e do nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="93bdf-121">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

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

### <span data-ttu-id="93bdf-122">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="93bdf-122">-VaultName</span></span>
<span data-ttu-id="93bdf-123">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="93bdf-123">Vault name.</span></span>
<span data-ttu-id="93bdf-124">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="93bdf-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="93bdf-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="93bdf-125">-Confirm</span></span>
<span data-ttu-id="93bdf-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93bdf-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93bdf-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93bdf-127">-WhatIf</span></span>
<span data-ttu-id="93bdf-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="93bdf-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93bdf-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="93bdf-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93bdf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93bdf-130">CommonParameters</span></span>
<span data-ttu-id="93bdf-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93bdf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93bdf-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93bdf-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93bdf-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="93bdf-133">INPUTS</span></span>

### <span data-ttu-id="93bdf-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="93bdf-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>
<span data-ttu-id="93bdf-135">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="93bdf-135">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="93bdf-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="93bdf-136">OUTPUTS</span></span>

### <span data-ttu-id="93bdf-137">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="93bdf-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="93bdf-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="93bdf-138">NOTES</span></span>

## <span data-ttu-id="93bdf-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="93bdf-139">RELATED LINKS</span></span>

[<span data-ttu-id="93bdf-140">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="93bdf-140">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="93bdf-141">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="93bdf-141">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)
