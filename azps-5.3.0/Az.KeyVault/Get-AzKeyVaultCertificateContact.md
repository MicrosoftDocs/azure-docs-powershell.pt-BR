---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
ms.openlocfilehash: ca7f0f87ebcbad3d613939f2e73a743763b134c9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429818"
---
# <span data-ttu-id="0dd05-101">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="0dd05-101">Get-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="0dd05-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0dd05-102">SYNOPSIS</span></span>
<span data-ttu-id="0dd05-103">Obtém contatos que são registrados para notificações de certificado para um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="0dd05-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

## <span data-ttu-id="0dd05-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0dd05-104">SYNTAX</span></span>

### <span data-ttu-id="0dd05-105">Cofrename (padrão)</span><span class="sxs-lookup"><span data-stu-id="0dd05-105">VaultName (Default)</span></span>
```
Get-AzKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0dd05-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0dd05-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0dd05-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0dd05-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0dd05-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0dd05-108">DESCRIPTION</span></span>
<span data-ttu-id="0dd05-109">O cmdlet **Get-AzKeyVaultCertificateContact** Obtém contatos que são registrados para notificações de certificado para um cofre de chaves no cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="0dd05-109">The **Get-AzKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="0dd05-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0dd05-110">EXAMPLES</span></span>

### <span data-ttu-id="0dd05-111">Exemplo 1: obter todos os contatos do certificado</span><span class="sxs-lookup"><span data-stu-id="0dd05-111">Example 1: Get all certificate contacts</span></span>
```powershell
PS C:\> $Contacts = Get-AzKeyVaultCertificateContact -VaultName "Contoso"

Email                   VaultName
-----                   ---------
username@microsoft.com  Contoso
username1@microsoft.com Contoso
```

<span data-ttu-id="0dd05-112">Esse comando obtém todos os contatos dos objetos de certificado no cofre de chaves da Contoso e os armazena na variável $Contacts.</span><span class="sxs-lookup"><span data-stu-id="0dd05-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="0dd05-113">OS</span><span class="sxs-lookup"><span data-stu-id="0dd05-113">PARAMETERS</span></span>

### <span data-ttu-id="0dd05-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dd05-114">-DefaultProfile</span></span>
<span data-ttu-id="0dd05-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0dd05-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0dd05-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0dd05-116">-InputObject</span></span>
<span data-ttu-id="0dd05-117">Objeto do keyvault.</span><span class="sxs-lookup"><span data-stu-id="0dd05-117">KeyVault object.</span></span>

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

### <span data-ttu-id="0dd05-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0dd05-118">-ResourceId</span></span>
<span data-ttu-id="0dd05-119">ID do keyvault.</span><span class="sxs-lookup"><span data-stu-id="0dd05-119">KeyVault Id.</span></span>

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

### <span data-ttu-id="0dd05-120">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="0dd05-120">-VaultName</span></span>
<span data-ttu-id="0dd05-121">Especifica o nome do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="0dd05-121">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="0dd05-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dd05-122">CommonParameters</span></span>
<span data-ttu-id="0dd05-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dd05-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dd05-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0dd05-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dd05-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0dd05-125">INPUTS</span></span>

### <span data-ttu-id="0dd05-126">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="0dd05-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="0dd05-127">System. String</span><span class="sxs-lookup"><span data-stu-id="0dd05-127">System.String</span></span>

## <span data-ttu-id="0dd05-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0dd05-128">OUTPUTS</span></span>

### <span data-ttu-id="0dd05-129">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="0dd05-129">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="0dd05-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0dd05-130">NOTES</span></span>

## <span data-ttu-id="0dd05-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0dd05-131">RELATED LINKS</span></span>

[<span data-ttu-id="0dd05-132">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="0dd05-132">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="0dd05-133">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="0dd05-133">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

