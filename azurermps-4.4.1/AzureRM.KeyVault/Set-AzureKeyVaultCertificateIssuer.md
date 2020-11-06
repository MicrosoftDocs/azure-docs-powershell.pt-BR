---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: eac75ae5c9828493244ace01b6c090fda7e6ef5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432207"
---
# <span data-ttu-id="066aa-101">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="066aa-101">Set-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="066aa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="066aa-102">SYNOPSIS</span></span>
<span data-ttu-id="066aa-103">Define um emissor de certificado em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="066aa-103">Sets a certificate issuer in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="066aa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="066aa-104">SYNTAX</span></span>

### <span data-ttu-id="066aa-105">Expandido (padrão)</span><span class="sxs-lookup"><span data-stu-id="066aa-105">Expanded (Default)</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-IssuerProvider <String>]
 [-AccountId <String>] [-ApiKey <SecureString>] [-OrganizationDetails <KeyVaultCertificateOrganizationDetails>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="066aa-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="066aa-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -Issuer <KeyVaultCertificateIssuer>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="066aa-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="066aa-107">DESCRIPTION</span></span>
<span data-ttu-id="066aa-108">O cmdlet Set-AzureKeyVaultCertificateIssuer define um emissor de certificado em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="066aa-108">The Set-AzureKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="066aa-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="066aa-109">EXAMPLES</span></span>

### <span data-ttu-id="066aa-110">Exemplo 1: definir um emissor de certificado</span><span class="sxs-lookup"><span data-stu-id="066aa-110">Example 1: Set a certificate issuer</span></span>
```
PS C:\>$Issuer = Set-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru
```

<span data-ttu-id="066aa-111">Esse comando define as propriedades de um emissor de certificado e, em seguida, armazena-o na variável $Issuer.</span><span class="sxs-lookup"><span data-stu-id="066aa-111">This command sets the properties for a certificate issuer, and then stores it in the $Issuer variable.</span></span>

## <span data-ttu-id="066aa-112">OS</span><span class="sxs-lookup"><span data-stu-id="066aa-112">PARAMETERS</span></span>

### <span data-ttu-id="066aa-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="066aa-113">-AccountId</span></span>
<span data-ttu-id="066aa-114">Especifica a ID da conta para o emissor do certificado.</span><span class="sxs-lookup"><span data-stu-id="066aa-114">Specifies the account ID for the certificate issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="066aa-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="066aa-115">-ApiKey</span></span>
<span data-ttu-id="066aa-116">Especifica a chave de API para o emissor do certificado.</span><span class="sxs-lookup"><span data-stu-id="066aa-116">Specifies the API key for the certificate issuer.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="066aa-117">-Emissor</span><span class="sxs-lookup"><span data-stu-id="066aa-117">-Issuer</span></span>
<span data-ttu-id="066aa-118">Especifica o emissor do certificado a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="066aa-118">Specifies the certificate issuer to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer
Parameter Sets: ByValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="066aa-119">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="066aa-119">-IssuerProvider</span></span>
<span data-ttu-id="066aa-120">Especifica o tipo de emissor do certificado.</span><span class="sxs-lookup"><span data-stu-id="066aa-120">Specifies the type of certificate issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="066aa-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="066aa-121">-Name</span></span>
<span data-ttu-id="066aa-122">Especifica o nome do emissor.</span><span class="sxs-lookup"><span data-stu-id="066aa-122">Specifies the name of the Issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="066aa-123">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="066aa-123">-OrganizationDetails</span></span>
<span data-ttu-id="066aa-124">Detalhes da organização a serem usados com o emissor.</span><span class="sxs-lookup"><span data-stu-id="066aa-124">Organization details to be used with the issuer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="066aa-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="066aa-125">-PassThru</span></span>
<span data-ttu-id="066aa-126">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="066aa-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="066aa-127">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="066aa-127">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="066aa-128">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="066aa-128">-VaultName</span></span>
<span data-ttu-id="066aa-129">Especifica o nome do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="066aa-129">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="066aa-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="066aa-130">-Confirm</span></span>
<span data-ttu-id="066aa-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="066aa-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="066aa-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="066aa-132">-WhatIf</span></span>
<span data-ttu-id="066aa-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="066aa-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="066aa-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="066aa-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="066aa-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="066aa-135">-DefaultProfile</span></span>
<span data-ttu-id="066aa-136">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="066aa-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="066aa-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="066aa-137">CommonParameters</span></span>
<span data-ttu-id="066aa-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="066aa-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="066aa-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="066aa-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="066aa-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="066aa-140">INPUTS</span></span>

## <span data-ttu-id="066aa-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="066aa-141">OUTPUTS</span></span>

### <span data-ttu-id="066aa-142">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="066aa-142">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="066aa-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="066aa-143">NOTES</span></span>

## <span data-ttu-id="066aa-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="066aa-144">RELATED LINKS</span></span>

[<span data-ttu-id="066aa-145">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="066aa-145">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="066aa-146">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="066aa-146">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

