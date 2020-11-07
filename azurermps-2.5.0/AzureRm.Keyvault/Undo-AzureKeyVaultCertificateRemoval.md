---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultcertificateremoval
schema: 2.0.0
ms.openlocfilehash: 493d4bcd641e8132bffd49100a04732759ce7e91
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785749"
---
# <span data-ttu-id="95bbc-101">Undo-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="95bbc-101">Undo-AzureKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="95bbc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="95bbc-102">SYNOPSIS</span></span>
<span data-ttu-id="95bbc-103">Recupera um certificado excluído em um cofre de chaves para um estado ativo.</span><span class="sxs-lookup"><span data-stu-id="95bbc-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95bbc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95bbc-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95bbc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="95bbc-105">DESCRIPTION</span></span>
<span data-ttu-id="95bbc-106">O cmdlet **Undo-AzureKeyVaultCertificateRemoval** irá recuperar um certificado excluído anteriormente.</span><span class="sxs-lookup"><span data-stu-id="95bbc-106">The **Undo-AzureKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="95bbc-107">O certificado recuperado estará ativo e poderá ser usado para todas as operações.</span><span class="sxs-lookup"><span data-stu-id="95bbc-107">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="95bbc-108">O chamador precisa ter a permissão ' recuperar ' para executar essa operação.</span><span class="sxs-lookup"><span data-stu-id="95bbc-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="95bbc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="95bbc-109">EXAMPLES</span></span>

### <span data-ttu-id="95bbc-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="95bbc-110">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'
```

<span data-ttu-id="95bbc-111">Esse comando recuperará o certificado ' myCertificate ' que foi excluído anteriormente em um estado ativo e utilizável.</span><span class="sxs-lookup"><span data-stu-id="95bbc-111">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="95bbc-112">OS</span><span class="sxs-lookup"><span data-stu-id="95bbc-112">PARAMETERS</span></span>

### <span data-ttu-id="95bbc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95bbc-113">-DefaultProfile</span></span>
<span data-ttu-id="95bbc-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="95bbc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95bbc-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="95bbc-115">-Name</span></span>
<span data-ttu-id="95bbc-116">Nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="95bbc-116">Certificate name.</span></span>
<span data-ttu-id="95bbc-117">O cmdlet constrói o FQDN de um certificado a partir do nome do cofre, do ambiente selecionado no momento e do nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="95bbc-117">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95bbc-118">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="95bbc-118">-VaultName</span></span>
<span data-ttu-id="95bbc-119">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="95bbc-119">Vault name.</span></span>
<span data-ttu-id="95bbc-120">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="95bbc-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95bbc-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="95bbc-121">-Confirm</span></span>
<span data-ttu-id="95bbc-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95bbc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95bbc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95bbc-123">-WhatIf</span></span>
<span data-ttu-id="95bbc-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="95bbc-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95bbc-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="95bbc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95bbc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95bbc-126">CommonParameters</span></span>
<span data-ttu-id="95bbc-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95bbc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95bbc-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95bbc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95bbc-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="95bbc-129">INPUTS</span></span>

### <span data-ttu-id="95bbc-130">System. String</span><span class="sxs-lookup"><span data-stu-id="95bbc-130">System.String</span></span>

## <span data-ttu-id="95bbc-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="95bbc-131">OUTPUTS</span></span>

### <span data-ttu-id="95bbc-132">Microsoft. Azure. Commands. keyvault. Models. Certificate</span><span class="sxs-lookup"><span data-stu-id="95bbc-132">Microsoft.Azure.Commands.KeyVault.Models.Certificate</span></span>

## <span data-ttu-id="95bbc-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="95bbc-133">NOTES</span></span>

## <span data-ttu-id="95bbc-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="95bbc-134">RELATED LINKS</span></span>

[<span data-ttu-id="95bbc-135">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="95bbc-135">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="95bbc-136">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="95bbc-136">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)
