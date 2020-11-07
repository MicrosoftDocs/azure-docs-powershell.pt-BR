---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
ms.openlocfilehash: e02b60055818d1ed79e93e6853353795e78c5830
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775805"
---
# <span data-ttu-id="3a25d-101">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="3a25d-101">Get-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="3a25d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3a25d-102">SYNOPSIS</span></span>
<span data-ttu-id="3a25d-103">Obtém contatos que são registrados para notificações de certificado para um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="3a25d-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

## <span data-ttu-id="3a25d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a25d-104">SYNTAX</span></span>

```
Get-AzKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3a25d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3a25d-105">DESCRIPTION</span></span>
<span data-ttu-id="3a25d-106">O cmdlet **Get-AzKeyVaultCertificateContact** Obtém contatos que são registrados para notificações de certificado para um cofre de chaves no cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="3a25d-106">The **Get-AzKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="3a25d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3a25d-107">EXAMPLES</span></span>

### <span data-ttu-id="3a25d-108">Exemplo 1: obter todos os contatos do certificado</span><span class="sxs-lookup"><span data-stu-id="3a25d-108">Example 1: Get all certificate contacts</span></span>
```
PS C:\>$Contacts = Get-AzKeyVaultCertificateContact -VaultName "Contoso"
```

<span data-ttu-id="3a25d-109">Esse comando obtém todos os contatos dos objetos de certificado no cofre de chaves da Contoso e os armazena na variável $Contacts.</span><span class="sxs-lookup"><span data-stu-id="3a25d-109">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="3a25d-110">OS</span><span class="sxs-lookup"><span data-stu-id="3a25d-110">PARAMETERS</span></span>

### <span data-ttu-id="3a25d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a25d-111">-DefaultProfile</span></span>
<span data-ttu-id="3a25d-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3a25d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a25d-113">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="3a25d-113">-VaultName</span></span>
<span data-ttu-id="3a25d-114">Especifica o nome do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="3a25d-114">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="3a25d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a25d-115">CommonParameters</span></span>
<span data-ttu-id="3a25d-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a25d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a25d-117">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a25d-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a25d-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3a25d-118">INPUTS</span></span>

### <span data-ttu-id="3a25d-119">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3a25d-119">None</span></span>
<span data-ttu-id="3a25d-120">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="3a25d-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3a25d-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3a25d-121">OUTPUTS</span></span>

### <span data-ttu-id="3a25d-122">List<Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="3a25d-122">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="3a25d-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3a25d-123">NOTES</span></span>

## <span data-ttu-id="3a25d-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3a25d-124">RELATED LINKS</span></span>

[<span data-ttu-id="3a25d-125">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="3a25d-125">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="3a25d-126">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="3a25d-126">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

