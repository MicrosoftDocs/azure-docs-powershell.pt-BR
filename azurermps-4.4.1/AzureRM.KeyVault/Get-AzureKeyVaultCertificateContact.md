---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: 6a59b49da2ae283af50487bec21da6c1d2457878
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610002"
---
# <span data-ttu-id="49494-101">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="49494-101">Get-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="49494-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="49494-102">SYNOPSIS</span></span>
<span data-ttu-id="49494-103">Obtém contatos que são registrados para notificações de certificado para um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="49494-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49494-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="49494-104">SYNTAX</span></span>

```
Get-AzureKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="49494-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="49494-105">DESCRIPTION</span></span>
<span data-ttu-id="49494-106">O cmdlet **Get-AzureKeyVaultCertificateContact** Obtém contatos que são registrados para notificações de certificado para um cofre de chaves no cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="49494-106">The **Get-AzureKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="49494-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="49494-107">EXAMPLES</span></span>

### <span data-ttu-id="49494-108">Exemplo 1: obter todos os contatos do certificado</span><span class="sxs-lookup"><span data-stu-id="49494-108">Example 1: Get all certificate contacts</span></span>
```
PS C:\>$Contacts = Get-AzureKeyVaultCertificateContact -VaultName "Contoso"
```

<span data-ttu-id="49494-109">Esse comando obtém todos os contatos dos objetos de certificado no cofre de chaves da Contoso e os armazena na variável $Contacts.</span><span class="sxs-lookup"><span data-stu-id="49494-109">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="49494-110">OS</span><span class="sxs-lookup"><span data-stu-id="49494-110">PARAMETERS</span></span>

### <span data-ttu-id="49494-111">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="49494-111">-VaultName</span></span>
<span data-ttu-id="49494-112">Especifica o nome do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="49494-112">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49494-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49494-113">-DefaultProfile</span></span>
<span data-ttu-id="49494-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="49494-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49494-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49494-115">CommonParameters</span></span>
<span data-ttu-id="49494-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49494-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49494-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49494-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49494-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="49494-118">INPUTS</span></span>

## <span data-ttu-id="49494-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="49494-119">OUTPUTS</span></span>

### <span data-ttu-id="49494-120">List<Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="49494-120">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="49494-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="49494-121">NOTES</span></span>

## <span data-ttu-id="49494-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="49494-122">RELATED LINKS</span></span>

[<span data-ttu-id="49494-123">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="49494-123">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="49494-124">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="49494-124">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

