---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
ms.openlocfilehash: ca7f0f87ebcbad3d613939f2e73a743763b134c9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113764"
---
# <span data-ttu-id="ef795-101">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="ef795-101">Get-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="ef795-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ef795-102">SYNOPSIS</span></span>
<span data-ttu-id="ef795-103">Obtém contatos registrados para notificações de certificado para um cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="ef795-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

## <span data-ttu-id="ef795-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ef795-104">SYNTAX</span></span>

### <span data-ttu-id="ef795-105">Nomedo Cofre (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ef795-105">VaultName (Default)</span></span>
```
Get-AzKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ef795-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ef795-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ef795-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ef795-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ef795-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ef795-108">DESCRIPTION</span></span>
<span data-ttu-id="ef795-109">O cmdlet **Get-AzKeyVaultCertificateContact** obtém contatos registrados para notificações de certificado para um cofre de chave no Cofre de Teclas do Azure.</span><span class="sxs-lookup"><span data-stu-id="ef795-109">The **Get-AzKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="ef795-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ef795-110">EXAMPLES</span></span>

### <span data-ttu-id="ef795-111">Exemplo 1: Obter todos os contatos de certificado</span><span class="sxs-lookup"><span data-stu-id="ef795-111">Example 1: Get all certificate contacts</span></span>
```powershell
PS C:\> $Contacts = Get-AzKeyVaultCertificateContact -VaultName "Contoso"

Email                   VaultName
-----                   ---------
username@microsoft.com  Contoso
username1@microsoft.com Contoso
```

<span data-ttu-id="ef795-112">Esse comando obtém todos os contatos dos objetos de certificado no cofre de teclas contoso e os armazena na variável $Contacts dados.</span><span class="sxs-lookup"><span data-stu-id="ef795-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="ef795-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ef795-113">PARAMETERS</span></span>

### <span data-ttu-id="ef795-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef795-114">-DefaultProfile</span></span>
<span data-ttu-id="ef795-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="ef795-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef795-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef795-116">-InputObject</span></span>
<span data-ttu-id="ef795-117">Objeto KeyVault.</span><span class="sxs-lookup"><span data-stu-id="ef795-117">KeyVault object.</span></span>

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

### <span data-ttu-id="ef795-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef795-118">-ResourceId</span></span>
<span data-ttu-id="ef795-119">ID do KeyVault.</span><span class="sxs-lookup"><span data-stu-id="ef795-119">KeyVault Id.</span></span>

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

### <span data-ttu-id="ef795-120">-Nomedo Cofre</span><span class="sxs-lookup"><span data-stu-id="ef795-120">-VaultName</span></span>
<span data-ttu-id="ef795-121">Especifica o nome do cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="ef795-121">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="ef795-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef795-122">CommonParameters</span></span>
<span data-ttu-id="ef795-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef795-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef795-124">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef795-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef795-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="ef795-125">INPUTS</span></span>

### <span data-ttu-id="ef795-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="ef795-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="ef795-127">System.String</span><span class="sxs-lookup"><span data-stu-id="ef795-127">System.String</span></span>

## <span data-ttu-id="ef795-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="ef795-128">OUTPUTS</span></span>

### <span data-ttu-id="ef795-129">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="ef795-129">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="ef795-130">Notas</span><span class="sxs-lookup"><span data-stu-id="ef795-130">NOTES</span></span>

## <span data-ttu-id="ef795-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ef795-131">RELATED LINKS</span></span>

[<span data-ttu-id="ef795-132">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="ef795-132">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="ef795-133">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="ef795-133">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

