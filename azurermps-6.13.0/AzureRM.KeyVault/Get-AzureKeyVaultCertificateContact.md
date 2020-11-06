---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: 31619366c1d2a1a025cb7ff563a04b166abb2a46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609795"
---
# <span data-ttu-id="2b5d7-101">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="2b5d7-101">Get-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="2b5d7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2b5d7-102">SYNOPSIS</span></span>
<span data-ttu-id="2b5d7-103">Obtém contatos que são registrados para notificações de certificado para um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="2b5d7-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b5d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2b5d7-104">SYNTAX</span></span>

### <span data-ttu-id="2b5d7-105">Cofrename (padrão)</span><span class="sxs-lookup"><span data-stu-id="2b5d7-105">VaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b5d7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2b5d7-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b5d7-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2b5d7-107">ByResourceId</span></span>
```
Get-AzureKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2b5d7-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2b5d7-108">DESCRIPTION</span></span>
<span data-ttu-id="2b5d7-109">O cmdlet **Get-AzureKeyVaultCertificateContact** Obtém contatos que são registrados para notificações de certificado para um cofre de chaves no cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="2b5d7-109">The **Get-AzureKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="2b5d7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2b5d7-110">EXAMPLES</span></span>

### <span data-ttu-id="2b5d7-111">Exemplo 1: obter todos os contatos do certificado</span><span class="sxs-lookup"><span data-stu-id="2b5d7-111">Example 1: Get all certificate contacts</span></span>
```powershell
PS C:\> $Contacts = Get-AzureKeyVaultCertificateContact -VaultName "Contoso"

Email                   VaultName
-----                   ---------
username@microsoft.com  Contoso
username1@microsoft.com Contoso
```

<span data-ttu-id="2b5d7-112">Esse comando obtém todos os contatos dos objetos de certificado no cofre de chaves da Contoso e os armazena na variável $Contacts.</span><span class="sxs-lookup"><span data-stu-id="2b5d7-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="2b5d7-113">OS</span><span class="sxs-lookup"><span data-stu-id="2b5d7-113">PARAMETERS</span></span>

### <span data-ttu-id="2b5d7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b5d7-114">-DefaultProfile</span></span>
<span data-ttu-id="2b5d7-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2b5d7-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2b5d7-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b5d7-116">-InputObject</span></span>
<span data-ttu-id="2b5d7-117">Objeto do keyvault.</span><span class="sxs-lookup"><span data-stu-id="2b5d7-117">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b5d7-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b5d7-118">-ResourceId</span></span>
<span data-ttu-id="2b5d7-119">ID do keyvault.</span><span class="sxs-lookup"><span data-stu-id="2b5d7-119">KeyVault Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b5d7-120">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="2b5d7-120">-VaultName</span></span>
<span data-ttu-id="2b5d7-121">Especifica o nome do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="2b5d7-121">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: VaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b5d7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b5d7-122">CommonParameters</span></span>
<span data-ttu-id="2b5d7-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b5d7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b5d7-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b5d7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b5d7-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2b5d7-125">INPUTS</span></span>

### <span data-ttu-id="2b5d7-126">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="2b5d7-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="2b5d7-127">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2b5d7-127">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="2b5d7-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2b5d7-128">System.String</span></span>

## <span data-ttu-id="2b5d7-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2b5d7-129">OUTPUTS</span></span>

### <span data-ttu-id="2b5d7-130">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="2b5d7-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="2b5d7-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2b5d7-131">NOTES</span></span>

## <span data-ttu-id="2b5d7-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2b5d7-132">RELATED LINKS</span></span>

[<span data-ttu-id="2b5d7-133">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="2b5d7-133">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="2b5d7-134">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="2b5d7-134">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

