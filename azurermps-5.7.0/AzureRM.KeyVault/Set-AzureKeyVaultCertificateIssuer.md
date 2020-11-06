---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 2a79f4bb555576414b4ed14c06ee0050133e139d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440859"
---
# <span data-ttu-id="99254-101">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="99254-101">Set-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="99254-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="99254-102">SYNOPSIS</span></span>
<span data-ttu-id="99254-103">Define um emissor de certificado em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="99254-103">Sets a certificate issuer in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99254-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99254-104">SYNTAX</span></span>

### <span data-ttu-id="99254-105">Expandido (padrão)</span><span class="sxs-lookup"><span data-stu-id="99254-105">Expanded (Default)</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-IssuerProvider <String>]
 [-AccountId <String>] [-ApiKey <SecureString>]
 [-OrganizationDetails <PSKeyVaultCertificateOrganizationDetails>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99254-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="99254-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 -InputObject <PSKeyVaultCertificateIssuerIdentityItem> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99254-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="99254-107">DESCRIPTION</span></span>
<span data-ttu-id="99254-108">O cmdlet Set-AzureKeyVaultCertificateIssuer define um emissor de certificado em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="99254-108">The Set-AzureKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="99254-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="99254-109">EXAMPLES</span></span>

### <span data-ttu-id="99254-110">Exemplo 1: definir um emissor de certificado</span><span class="sxs-lookup"><span data-stu-id="99254-110">Example 1: Set a certificate issuer</span></span>
```
PS C:\>$Issuer = Set-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru
```

<span data-ttu-id="99254-111">Esse comando define as propriedades de um emissor de certificado e, em seguida, armazena-o na variável $Issuer.</span><span class="sxs-lookup"><span data-stu-id="99254-111">This command sets the properties for a certificate issuer, and then stores it in the $Issuer variable.</span></span>

## <span data-ttu-id="99254-112">OS</span><span class="sxs-lookup"><span data-stu-id="99254-112">PARAMETERS</span></span>

### <span data-ttu-id="99254-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="99254-113">-AccountId</span></span>
<span data-ttu-id="99254-114">Especifica a ID da conta para o emissor do certificado.</span><span class="sxs-lookup"><span data-stu-id="99254-114">Specifies the account ID for the certificate issuer.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99254-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="99254-115">-ApiKey</span></span>
<span data-ttu-id="99254-116">Especifica a chave de API para o emissor do certificado.</span><span class="sxs-lookup"><span data-stu-id="99254-116">Specifies the API key for the certificate issuer.</span></span>

```yaml
Type: SecureString
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99254-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99254-117">-DefaultProfile</span></span>
<span data-ttu-id="99254-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="99254-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99254-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99254-119">-InputObject</span></span>
<span data-ttu-id="99254-120">Especifica o emissor do certificado a ser definido.</span><span class="sxs-lookup"><span data-stu-id="99254-120">Specifies the certificate issuer to set.</span></span>

```yaml
Type: PSKeyVaultCertificateIssuerIdentityItem
Parameter Sets: ByValue
Aliases: Issuer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99254-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="99254-121">-IssuerProvider</span></span>
<span data-ttu-id="99254-122">Especifica o tipo de emissor do certificado.</span><span class="sxs-lookup"><span data-stu-id="99254-122">Specifies the type of certificate issuer.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99254-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="99254-123">-Name</span></span>
<span data-ttu-id="99254-124">Especifica o nome do emissor.</span><span class="sxs-lookup"><span data-stu-id="99254-124">Specifies the name of the Issuer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99254-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="99254-125">-OrganizationDetails</span></span>
<span data-ttu-id="99254-126">Detalhes da organização a serem usados com o emissor.</span><span class="sxs-lookup"><span data-stu-id="99254-126">Organization details to be used with the issuer.</span></span>

```yaml
Type: PSKeyVaultCertificateOrganizationDetails
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99254-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99254-127">-PassThru</span></span>
<span data-ttu-id="99254-128">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="99254-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="99254-129">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="99254-129">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99254-130">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="99254-130">-VaultName</span></span>
<span data-ttu-id="99254-131">Especifica o nome do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="99254-131">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="99254-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="99254-132">-Confirm</span></span>
<span data-ttu-id="99254-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99254-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99254-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99254-134">-WhatIf</span></span>
<span data-ttu-id="99254-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="99254-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99254-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="99254-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99254-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99254-137">CommonParameters</span></span>
<span data-ttu-id="99254-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99254-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99254-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99254-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99254-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="99254-140">INPUTS</span></span>

### <span data-ttu-id="99254-141">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="99254-141">None</span></span>
<span data-ttu-id="99254-142">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="99254-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="99254-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="99254-143">OUTPUTS</span></span>

### <span data-ttu-id="99254-144">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="99254-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="99254-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="99254-145">NOTES</span></span>

## <span data-ttu-id="99254-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="99254-146">RELATED LINKS</span></span>

[<span data-ttu-id="99254-147">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="99254-147">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="99254-148">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="99254-148">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

