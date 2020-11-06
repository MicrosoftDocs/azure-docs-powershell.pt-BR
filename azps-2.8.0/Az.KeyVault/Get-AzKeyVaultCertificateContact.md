---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 9c7b82c8ec884cc16bc3c593d9f00f1789b98e52
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596204"
---
# <span data-ttu-id="5d917-101">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="5d917-101">Get-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="5d917-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5d917-102">SYNOPSIS</span></span>
<span data-ttu-id="5d917-103">Obtém contatos que são registrados para notificações de certificado para um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="5d917-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

## <span data-ttu-id="5d917-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5d917-104">SYNTAX</span></span>

### <span data-ttu-id="5d917-105">Cofrename (padrão)</span><span class="sxs-lookup"><span data-stu-id="5d917-105">VaultName (Default)</span></span>
```
Get-AzKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5d917-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5d917-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5d917-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5d917-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5d917-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5d917-108">DESCRIPTION</span></span>
<span data-ttu-id="5d917-109">O cmdlet **Get-AzKeyVaultCertificateContact** Obtém contatos que são registrados para notificações de certificado para um cofre de chaves no cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="5d917-109">The **Get-AzKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="5d917-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5d917-110">EXAMPLES</span></span>

### <span data-ttu-id="5d917-111">Exemplo 1: obter todos os contatos do certificado</span><span class="sxs-lookup"><span data-stu-id="5d917-111">Example 1: Get all certificate contacts</span></span>
```powershell
PS C:\> $Contacts = Get-AzKeyVaultCertificateContact -VaultName "Contoso"

Email                   VaultName
-----                   ---------
username@microsoft.com  Contoso
username1@microsoft.com Contoso
```

<span data-ttu-id="5d917-112">Esse comando obtém todos os contatos dos objetos de certificado no cofre de chaves da Contoso e os armazena na variável $Contacts.</span><span class="sxs-lookup"><span data-stu-id="5d917-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="5d917-113">OS</span><span class="sxs-lookup"><span data-stu-id="5d917-113">PARAMETERS</span></span>

### <span data-ttu-id="5d917-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d917-114">-DefaultProfile</span></span>
<span data-ttu-id="5d917-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="5d917-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d917-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d917-116">-InputObject</span></span>
<span data-ttu-id="5d917-117">Objeto do keyvault.</span><span class="sxs-lookup"><span data-stu-id="5d917-117">KeyVault object.</span></span>

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

### <span data-ttu-id="5d917-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d917-118">-ResourceId</span></span>
<span data-ttu-id="5d917-119">ID do keyvault.</span><span class="sxs-lookup"><span data-stu-id="5d917-119">KeyVault Id.</span></span>

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

### <span data-ttu-id="5d917-120">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="5d917-120">-VaultName</span></span>
<span data-ttu-id="5d917-121">Especifica o nome do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="5d917-121">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="5d917-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d917-122">CommonParameters</span></span>
<span data-ttu-id="5d917-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d917-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d917-124">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d917-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d917-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5d917-125">INPUTS</span></span>

### <span data-ttu-id="5d917-126">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="5d917-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="5d917-127">System. String</span><span class="sxs-lookup"><span data-stu-id="5d917-127">System.String</span></span>

## <span data-ttu-id="5d917-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5d917-128">OUTPUTS</span></span>

### <span data-ttu-id="5d917-129">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="5d917-129">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="5d917-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5d917-130">NOTES</span></span>

## <span data-ttu-id="5d917-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5d917-131">RELATED LINKS</span></span>

[<span data-ttu-id="5d917-132">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="5d917-132">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="5d917-133">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="5d917-133">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

