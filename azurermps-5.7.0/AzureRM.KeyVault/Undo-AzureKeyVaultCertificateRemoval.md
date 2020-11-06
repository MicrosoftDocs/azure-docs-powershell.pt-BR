---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultcertificateremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
ms.openlocfilehash: 33024ce7002975848a98ff8bdfd6188196a96e6f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610390"
---
# <span data-ttu-id="1909b-101">Undo-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="1909b-101">Undo-AzureKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="1909b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1909b-102">SYNOPSIS</span></span>
<span data-ttu-id="1909b-103">Recupera um certificado excluído em um cofre de chaves para um estado ativo.</span><span class="sxs-lookup"><span data-stu-id="1909b-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1909b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1909b-104">SYNTAX</span></span>

### <span data-ttu-id="1909b-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="1909b-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1909b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="1909b-106">InputObject</span></span>
```
Undo-AzureKeyVaultCertificateRemoval [-InputObject] <PSDeletedKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1909b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1909b-107">DESCRIPTION</span></span>
<span data-ttu-id="1909b-108">O cmdlet **Undo-AzureKeyVaultCertificateRemoval** irá recuperar um certificado excluído anteriormente.</span><span class="sxs-lookup"><span data-stu-id="1909b-108">The **Undo-AzureKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="1909b-109">O certificado recuperado estará ativo e poderá ser usado para todas as operações.</span><span class="sxs-lookup"><span data-stu-id="1909b-109">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="1909b-110">O chamador precisa ter a permissão ' recuperar ' para executar essa operação.</span><span class="sxs-lookup"><span data-stu-id="1909b-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="1909b-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1909b-111">EXAMPLES</span></span>

### <span data-ttu-id="1909b-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1909b-112">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'
```

<span data-ttu-id="1909b-113">Esse comando recuperará o certificado ' myCertificate ' que foi excluído anteriormente em um estado ativo e utilizável.</span><span class="sxs-lookup"><span data-stu-id="1909b-113">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="1909b-114">OS</span><span class="sxs-lookup"><span data-stu-id="1909b-114">PARAMETERS</span></span>

### <span data-ttu-id="1909b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1909b-115">-DefaultProfile</span></span>
<span data-ttu-id="1909b-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="1909b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1909b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1909b-117">-InputObject</span></span>
<span data-ttu-id="1909b-118">Objeto de certificado excluído</span><span class="sxs-lookup"><span data-stu-id="1909b-118">Deleted Certificate object</span></span>

```yaml
Type: PSDeletedKeyVaultCertificateIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1909b-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="1909b-119">-Name</span></span>
<span data-ttu-id="1909b-120">Nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="1909b-120">Certificate name.</span></span>
<span data-ttu-id="1909b-121">O cmdlet constrói o FQDN de um certificado a partir do nome do cofre, do ambiente selecionado no momento e do nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="1909b-121">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1909b-122">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="1909b-122">-VaultName</span></span>
<span data-ttu-id="1909b-123">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="1909b-123">Vault name.</span></span>
<span data-ttu-id="1909b-124">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="1909b-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1909b-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1909b-125">-Confirm</span></span>
<span data-ttu-id="1909b-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1909b-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1909b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1909b-127">-WhatIf</span></span>
<span data-ttu-id="1909b-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1909b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1909b-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1909b-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1909b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1909b-130">CommonParameters</span></span>
<span data-ttu-id="1909b-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1909b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1909b-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1909b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1909b-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1909b-133">INPUTS</span></span>

### <span data-ttu-id="1909b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1909b-134">System.String</span></span>

## <span data-ttu-id="1909b-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1909b-135">OUTPUTS</span></span>

### <span data-ttu-id="1909b-136">Microsoft. Azure. Commands. keyvault. Models. CertificateBundle</span><span class="sxs-lookup"><span data-stu-id="1909b-136">Microsoft.Azure.Commands.KeyVault.Models.CertificateBundle</span></span>

## <span data-ttu-id="1909b-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1909b-137">NOTES</span></span>

## <span data-ttu-id="1909b-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1909b-138">RELATED LINKS</span></span>

[<span data-ttu-id="1909b-139">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="1909b-139">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="1909b-140">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="1909b-140">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)
