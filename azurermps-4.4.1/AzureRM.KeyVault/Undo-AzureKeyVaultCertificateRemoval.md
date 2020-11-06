---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultCertificateRemoval.md
ms.openlocfilehash: 91fee65a201de8babc7ef7aa09973f1e98f95cb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440626"
---
# <span data-ttu-id="12410-101">Undo-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="12410-101">Undo-AzureKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="12410-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="12410-102">SYNOPSIS</span></span>
<span data-ttu-id="12410-103">Recupera um certificado excluído em um cofre de chaves para um estado ativo.</span><span class="sxs-lookup"><span data-stu-id="12410-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12410-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12410-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12410-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="12410-105">DESCRIPTION</span></span>
<span data-ttu-id="12410-106">O cmdlet **Undo-AzureKeyVaultCertificateRemoval** irá recuperar um certificado excluído anteriormente.</span><span class="sxs-lookup"><span data-stu-id="12410-106">The **Undo-AzureKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="12410-107">O certificado recuperado estará ativo e poderá ser usado para todas as operações.</span><span class="sxs-lookup"><span data-stu-id="12410-107">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="12410-108">O chamador precisa ter a permissão ' recuperar ' para executar essa operação.</span><span class="sxs-lookup"><span data-stu-id="12410-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="12410-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12410-109">EXAMPLES</span></span>

### <span data-ttu-id="12410-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="12410-110">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'
```

<span data-ttu-id="12410-111">Esse comando recuperará o certificado ' myCertificate ' que foi excluído anteriormente em um estado ativo e utilizável.</span><span class="sxs-lookup"><span data-stu-id="12410-111">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="12410-112">OS</span><span class="sxs-lookup"><span data-stu-id="12410-112">PARAMETERS</span></span>

### <span data-ttu-id="12410-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="12410-113">-Name</span></span>
<span data-ttu-id="12410-114">Nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="12410-114">Certificate name.</span></span>
<span data-ttu-id="12410-115">O cmdlet constrói o FQDN de um certificado a partir do nome do cofre, do ambiente selecionado no momento e do nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="12410-115">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12410-116">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="12410-116">-VaultName</span></span>
<span data-ttu-id="12410-117">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="12410-117">Vault name.</span></span>
<span data-ttu-id="12410-118">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="12410-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12410-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="12410-119">-Confirm</span></span>
<span data-ttu-id="12410-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12410-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12410-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12410-121">-WhatIf</span></span>
<span data-ttu-id="12410-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="12410-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12410-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="12410-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12410-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12410-124">-DefaultProfile</span></span>
<span data-ttu-id="12410-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="12410-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12410-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12410-126">CommonParameters</span></span>
<span data-ttu-id="12410-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12410-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12410-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12410-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12410-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="12410-129">INPUTS</span></span>

### <span data-ttu-id="12410-130">System. String</span><span class="sxs-lookup"><span data-stu-id="12410-130">System.String</span></span>

## <span data-ttu-id="12410-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="12410-131">OUTPUTS</span></span>

### <span data-ttu-id="12410-132">Microsoft. Azure. Commands. keyvault. Models. Certificate</span><span class="sxs-lookup"><span data-stu-id="12410-132">Microsoft.Azure.Commands.KeyVault.Models.Certificate</span></span>

## <span data-ttu-id="12410-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="12410-133">NOTES</span></span>

## <span data-ttu-id="12410-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12410-134">RELATED LINKS</span></span>

[<span data-ttu-id="12410-135">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="12410-135">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="12410-136">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="12410-136">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)
