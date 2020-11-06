---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 05a59e3fd098fb32122cc85a4d39e89cf1fc66aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602524"
---
# <span data-ttu-id="988bb-101">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="988bb-101">Remove-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="988bb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="988bb-102">SYNOPSIS</span></span>
<span data-ttu-id="988bb-103">Exclui um emissor de certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="988bb-103">Deletes a certificate issuer from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="988bb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="988bb-104">SYNTAX</span></span>

### <span data-ttu-id="988bb-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="988bb-105">Default (Default)</span></span>
```
Remove-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="988bb-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="988bb-106">InputObject</span></span>
```
Remove-AzureKeyVaultCertificateIssuer [-InputObject] <PSKeyVaultCertificateIssuerIdentityItem> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="988bb-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="988bb-107">DESCRIPTION</span></span>
<span data-ttu-id="988bb-108">O cmdlet **Remove-AzureKeyVaultCertificateIssuer** exclui um emissor de certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="988bb-108">The **Remove-AzureKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="988bb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="988bb-109">EXAMPLES</span></span>

### <span data-ttu-id="988bb-110">Exemplo 1: remover um emissor de certificado</span><span class="sxs-lookup"><span data-stu-id="988bb-110">Example 1: Remove a certificate issuer</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force
```

<span data-ttu-id="988bb-111">Esse comando Remove o emissor do certificado chamado TestIssuer01 do cofre da chave ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="988bb-111">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="988bb-112">OS</span><span class="sxs-lookup"><span data-stu-id="988bb-112">PARAMETERS</span></span>

### <span data-ttu-id="988bb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="988bb-113">-DefaultProfile</span></span>
<span data-ttu-id="988bb-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="988bb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="988bb-115">-Force</span><span class="sxs-lookup"><span data-stu-id="988bb-115">-Force</span></span>
<span data-ttu-id="988bb-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="988bb-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="988bb-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="988bb-117">-InputObject</span></span>
<span data-ttu-id="988bb-118">Objeto emissor do certificado</span><span class="sxs-lookup"><span data-stu-id="988bb-118">Certificate Issuer Object</span></span>

```yaml
Type: PSKeyVaultCertificateIssuerIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="988bb-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="988bb-119">-Name</span></span>
<span data-ttu-id="988bb-120">Especifica o nome do emissor que será removido.</span><span class="sxs-lookup"><span data-stu-id="988bb-120">Specifies the name of the issuer to remove.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="988bb-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="988bb-121">-PassThru</span></span>
<span data-ttu-id="988bb-122">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="988bb-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="988bb-123">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="988bb-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="988bb-124">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="988bb-124">-VaultName</span></span>
<span data-ttu-id="988bb-125">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="988bb-125">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="988bb-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="988bb-126">-Confirm</span></span>
<span data-ttu-id="988bb-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="988bb-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="988bb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="988bb-128">-WhatIf</span></span>
<span data-ttu-id="988bb-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="988bb-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="988bb-130">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="988bb-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="988bb-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="988bb-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="988bb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="988bb-132">CommonParameters</span></span>
<span data-ttu-id="988bb-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="988bb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="988bb-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="988bb-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="988bb-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="988bb-135">INPUTS</span></span>

### <span data-ttu-id="988bb-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="988bb-136">None</span></span>
<span data-ttu-id="988bb-137">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="988bb-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="988bb-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="988bb-138">OUTPUTS</span></span>

### <span data-ttu-id="988bb-139">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="988bb-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="988bb-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="988bb-140">NOTES</span></span>

## <span data-ttu-id="988bb-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="988bb-141">RELATED LINKS</span></span>

[<span data-ttu-id="988bb-142">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="988bb-142">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="988bb-143">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="988bb-143">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


