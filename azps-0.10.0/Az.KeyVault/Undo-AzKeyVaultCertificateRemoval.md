---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/undo-AzKeyvaultcertificateremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
ms.openlocfilehash: 5757a9fb050d69cdf0ef0e648b0d446de1e3ee24
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775767"
---
# <span data-ttu-id="25c94-101">Undo-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="25c94-101">Undo-AzKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="25c94-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="25c94-102">SYNOPSIS</span></span>
<span data-ttu-id="25c94-103">Recupera um certificado excluído em um cofre de chaves para um estado ativo.</span><span class="sxs-lookup"><span data-stu-id="25c94-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

## <span data-ttu-id="25c94-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25c94-104">SYNTAX</span></span>

```
Undo-AzKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25c94-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="25c94-105">DESCRIPTION</span></span>
<span data-ttu-id="25c94-106">O cmdlet **Undo-AzKeyVaultCertificateRemoval** irá recuperar um certificado excluído anteriormente.</span><span class="sxs-lookup"><span data-stu-id="25c94-106">The **Undo-AzKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="25c94-107">O certificado recuperado estará ativo e poderá ser usado para todas as operações.</span><span class="sxs-lookup"><span data-stu-id="25c94-107">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="25c94-108">O chamador precisa ter a permissão ' recuperar ' para executar essa operação.</span><span class="sxs-lookup"><span data-stu-id="25c94-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="25c94-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="25c94-109">EXAMPLES</span></span>

### <span data-ttu-id="25c94-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="25c94-110">Example 1</span></span>
```
PS C:\> Undo-AzKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'
```

<span data-ttu-id="25c94-111">Esse comando recuperará o certificado ' myCertificate ' que foi excluído anteriormente em um estado ativo e utilizável.</span><span class="sxs-lookup"><span data-stu-id="25c94-111">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="25c94-112">OS</span><span class="sxs-lookup"><span data-stu-id="25c94-112">PARAMETERS</span></span>

### <span data-ttu-id="25c94-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25c94-113">-DefaultProfile</span></span>
<span data-ttu-id="25c94-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="25c94-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25c94-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="25c94-115">-Name</span></span>
<span data-ttu-id="25c94-116">Nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="25c94-116">Certificate name.</span></span>
<span data-ttu-id="25c94-117">O cmdlet constrói o FQDN de um certificado a partir do nome do cofre, do ambiente selecionado no momento e do nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="25c94-117">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

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

### <span data-ttu-id="25c94-118">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="25c94-118">-VaultName</span></span>
<span data-ttu-id="25c94-119">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="25c94-119">Vault name.</span></span>
<span data-ttu-id="25c94-120">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="25c94-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="25c94-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="25c94-121">-Confirm</span></span>
<span data-ttu-id="25c94-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25c94-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25c94-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25c94-123">-WhatIf</span></span>
<span data-ttu-id="25c94-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="25c94-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25c94-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="25c94-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25c94-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25c94-126">CommonParameters</span></span>
<span data-ttu-id="25c94-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25c94-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25c94-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25c94-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25c94-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="25c94-129">INPUTS</span></span>

### <span data-ttu-id="25c94-130">System. String</span><span class="sxs-lookup"><span data-stu-id="25c94-130">System.String</span></span>

## <span data-ttu-id="25c94-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="25c94-131">OUTPUTS</span></span>

### <span data-ttu-id="25c94-132">Microsoft. Azure. Commands. keyvault. Models. Certificate</span><span class="sxs-lookup"><span data-stu-id="25c94-132">Microsoft.Azure.Commands.KeyVault.Models.Certificate</span></span>

## <span data-ttu-id="25c94-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="25c94-133">NOTES</span></span>

## <span data-ttu-id="25c94-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25c94-134">RELATED LINKS</span></span>

[<span data-ttu-id="25c94-135">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="25c94-135">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="25c94-136">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="25c94-136">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)
