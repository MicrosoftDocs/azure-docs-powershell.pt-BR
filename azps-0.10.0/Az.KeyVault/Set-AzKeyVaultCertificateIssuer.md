---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 97faf51b25ee2ae36b028e4a6b992416949a219f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776654"
---
# <span data-ttu-id="f1c5e-101">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="f1c5e-101">Set-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="f1c5e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f1c5e-102">SYNOPSIS</span></span>
<span data-ttu-id="f1c5e-103">Define um emissor de certificado em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="f1c5e-103">Sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="f1c5e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1c5e-104">SYNTAX</span></span>

### <span data-ttu-id="f1c5e-105">Expandido (padrão)</span><span class="sxs-lookup"><span data-stu-id="f1c5e-105">Expanded (Default)</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-IssuerProvider <String>]
 [-AccountId <String>] [-ApiKey <SecureString>] [-OrganizationDetails <KeyVaultCertificateOrganizationDetails>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1c5e-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="f1c5e-106">ByValue</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -Issuer <KeyVaultCertificateIssuer>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1c5e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f1c5e-107">DESCRIPTION</span></span>
<span data-ttu-id="f1c5e-108">O cmdlet Set-AzKeyVaultCertificateIssuer define um emissor de certificado em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="f1c5e-108">The Set-AzKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="f1c5e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f1c5e-109">EXAMPLES</span></span>

### <span data-ttu-id="f1c5e-110">Exemplo 1: definir um emissor de certificado</span><span class="sxs-lookup"><span data-stu-id="f1c5e-110">Example 1: Set a certificate issuer</span></span>
```
PS C:\>$Issuer = Set-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru
```

<span data-ttu-id="f1c5e-111">Esse comando define as propriedades de um emissor de certificado e, em seguida, armazena-o na variável $Issuer.</span><span class="sxs-lookup"><span data-stu-id="f1c5e-111">This command sets the properties for a certificate issuer, and then stores it in the $Issuer variable.</span></span>

## <span data-ttu-id="f1c5e-112">OS</span><span class="sxs-lookup"><span data-stu-id="f1c5e-112">PARAMETERS</span></span>

### <span data-ttu-id="f1c5e-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="f1c5e-113">-AccountId</span></span>
<span data-ttu-id="f1c5e-114">Especifica a ID da conta para o emissor do certificado.</span><span class="sxs-lookup"><span data-stu-id="f1c5e-114">Specifies the account ID for the certificate issuer.</span></span>

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

### <span data-ttu-id="f1c5e-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="f1c5e-115">-ApiKey</span></span>
<span data-ttu-id="f1c5e-116">Especifica a chave de API para o emissor do certificado.</span><span class="sxs-lookup"><span data-stu-id="f1c5e-116">Specifies the API key for the certificate issuer.</span></span>

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

### <span data-ttu-id="f1c5e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1c5e-117">-DefaultProfile</span></span>
<span data-ttu-id="f1c5e-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f1c5e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1c5e-119">-Emissor</span><span class="sxs-lookup"><span data-stu-id="f1c5e-119">-Issuer</span></span>
<span data-ttu-id="f1c5e-120">Especifica o emissor do certificado a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="f1c5e-120">Specifies the certificate issuer to update.</span></span>

```yaml
Type: KeyVaultCertificateIssuer
Parameter Sets: ByValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1c5e-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="f1c5e-121">-IssuerProvider</span></span>
<span data-ttu-id="f1c5e-122">Especifica o tipo de emissor do certificado.</span><span class="sxs-lookup"><span data-stu-id="f1c5e-122">Specifies the type of certificate issuer.</span></span>

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

### <span data-ttu-id="f1c5e-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="f1c5e-123">-Name</span></span>
<span data-ttu-id="f1c5e-124">Especifica o nome do emissor.</span><span class="sxs-lookup"><span data-stu-id="f1c5e-124">Specifies the name of the Issuer.</span></span>

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

### <span data-ttu-id="f1c5e-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="f1c5e-125">-OrganizationDetails</span></span>
<span data-ttu-id="f1c5e-126">Detalhes da organização a serem usados com o emissor.</span><span class="sxs-lookup"><span data-stu-id="f1c5e-126">Organization details to be used with the issuer.</span></span>

```yaml
Type: KeyVaultCertificateOrganizationDetails
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1c5e-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1c5e-127">-PassThru</span></span>
<span data-ttu-id="f1c5e-128">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="f1c5e-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f1c5e-129">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="f1c5e-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f1c5e-130">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="f1c5e-130">-VaultName</span></span>
<span data-ttu-id="f1c5e-131">Especifica o nome do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="f1c5e-131">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="f1c5e-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f1c5e-132">-Confirm</span></span>
<span data-ttu-id="f1c5e-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1c5e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1c5e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1c5e-134">-WhatIf</span></span>
<span data-ttu-id="f1c5e-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f1c5e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1c5e-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f1c5e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1c5e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1c5e-137">CommonParameters</span></span>
<span data-ttu-id="f1c5e-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1c5e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1c5e-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1c5e-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1c5e-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f1c5e-140">INPUTS</span></span>

### <span data-ttu-id="f1c5e-141">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f1c5e-141">None</span></span>
<span data-ttu-id="f1c5e-142">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="f1c5e-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f1c5e-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f1c5e-143">OUTPUTS</span></span>

### <span data-ttu-id="f1c5e-144">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="f1c5e-144">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="f1c5e-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f1c5e-145">NOTES</span></span>

## <span data-ttu-id="f1c5e-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1c5e-146">RELATED LINKS</span></span>

[<span data-ttu-id="f1c5e-147">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="f1c5e-147">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="f1c5e-148">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="f1c5e-148">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

