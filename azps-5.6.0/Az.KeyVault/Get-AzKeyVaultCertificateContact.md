---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 4a8eb9ce6fce4cf9719e365055cab5743d081b1b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892157"
---
# <span data-ttu-id="5c399-101">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="5c399-101">Get-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="5c399-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c399-102">SYNOPSIS</span></span>
<span data-ttu-id="5c399-103">Obtém contatos registrados para notificações de certificado para um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="5c399-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

## <span data-ttu-id="5c399-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5c399-104">SYNTAX</span></span>

### <span data-ttu-id="5c399-105">VaultName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5c399-105">VaultName (Default)</span></span>
```
Get-AzKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5c399-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5c399-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5c399-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5c399-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5c399-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5c399-108">DESCRIPTION</span></span>
<span data-ttu-id="5c399-109">O cmdlet **Get-AzKeyVaultCertificateContact** obtém contatos registrados para notificações de certificado para um cofre de chaves no Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="5c399-109">The **Get-AzKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="5c399-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5c399-110">EXAMPLES</span></span>

### <span data-ttu-id="5c399-111">Exemplo 1: Obter todos os contatos de certificado</span><span class="sxs-lookup"><span data-stu-id="5c399-111">Example 1: Get all certificate contacts</span></span>
```powershell
PS C:\> $Contacts = Get-AzKeyVaultCertificateContact -VaultName "Contoso"

Email                   VaultName
-----                   ---------
username@microsoft.com  Contoso
username1@microsoft.com Contoso
```

<span data-ttu-id="5c399-112">Esse comando obtém todos os contatos dos objetos de certificado no cofre de chaves contoso e os armazena na variável $Contacts.</span><span class="sxs-lookup"><span data-stu-id="5c399-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="5c399-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5c399-113">PARAMETERS</span></span>

### <span data-ttu-id="5c399-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c399-114">-DefaultProfile</span></span>
<span data-ttu-id="5c399-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="5c399-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c399-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c399-116">-InputObject</span></span>
<span data-ttu-id="5c399-117">Objeto KeyVault.</span><span class="sxs-lookup"><span data-stu-id="5c399-117">KeyVault object.</span></span>

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

### <span data-ttu-id="5c399-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c399-118">-ResourceId</span></span>
<span data-ttu-id="5c399-119">KeyVault Id.</span><span class="sxs-lookup"><span data-stu-id="5c399-119">KeyVault Id.</span></span>

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

### <span data-ttu-id="5c399-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="5c399-120">-VaultName</span></span>
<span data-ttu-id="5c399-121">Especifica o nome do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="5c399-121">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="5c399-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c399-122">CommonParameters</span></span>
<span data-ttu-id="5c399-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c399-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c399-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c399-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c399-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5c399-125">INPUTS</span></span>

### <span data-ttu-id="5c399-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="5c399-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="5c399-127">System.String</span><span class="sxs-lookup"><span data-stu-id="5c399-127">System.String</span></span>

## <span data-ttu-id="5c399-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5c399-128">OUTPUTS</span></span>

### <span data-ttu-id="5c399-129">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="5c399-129">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="5c399-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="5c399-130">NOTES</span></span>

## <span data-ttu-id="5c399-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5c399-131">RELATED LINKS</span></span>

[<span data-ttu-id="5c399-132">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="5c399-132">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="5c399-133">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="5c399-133">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

