---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2659C06A-AE5B-4F7B-B9EF-069A74E12560
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateOperation.md
ms.openlocfilehash: 70d6d39ed3e2083bf0f52e9e56808b7d36f1cc24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429766"
---
# <span data-ttu-id="57c77-101">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="57c77-101">Remove-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="57c77-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="57c77-102">SYNOPSIS</span></span>
<span data-ttu-id="57c77-103">Exclui uma operação de certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="57c77-103">Deletes a certificate operation from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57c77-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="57c77-104">SYNTAX</span></span>

### <span data-ttu-id="57c77-105">Assume</span><span class="sxs-lookup"><span data-stu-id="57c77-105">Default</span></span>
```
Remove-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57c77-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="57c77-106">InputObject</span></span>
```
Remove-AzureKeyVaultCertificateOperation [-InputObject] <PSKeyVaultCertificateOperation> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57c77-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="57c77-107">DESCRIPTION</span></span>
<span data-ttu-id="57c77-108">O cmdlet **Remove-AzureKeyVaultCertificateOperation** exclui uma operação de certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="57c77-108">The **Remove-AzureKeyVaultCertificateOperation** cmdlet deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="57c77-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="57c77-109">EXAMPLES</span></span>

### <span data-ttu-id="57c77-110">Exemplo 1: remover uma operação de certificado</span><span class="sxs-lookup"><span data-stu-id="57c77-110">Example 1: Remove a certificate operation</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01" -Force
```

<span data-ttu-id="57c77-111">Esse comando Remove a operação de certificado chamada TestCert01 do cofre da chave ContosoKV01 sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="57c77-111">This command removes the certificate operation named TestCert01 from the ContosoKV01 key vault without prompting for confirmation.</span></span>

## <span data-ttu-id="57c77-112">OS</span><span class="sxs-lookup"><span data-stu-id="57c77-112">PARAMETERS</span></span>

### <span data-ttu-id="57c77-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57c77-113">-DefaultProfile</span></span>
<span data-ttu-id="57c77-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="57c77-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57c77-115">-Force</span><span class="sxs-lookup"><span data-stu-id="57c77-115">-Force</span></span>
<span data-ttu-id="57c77-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="57c77-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="57c77-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57c77-117">-InputObject</span></span>
<span data-ttu-id="57c77-118">Objeto Operation</span><span class="sxs-lookup"><span data-stu-id="57c77-118">Operation object</span></span>

```yaml
Type: PSKeyVaultCertificateOperation
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57c77-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="57c77-119">-Name</span></span>
<span data-ttu-id="57c77-120">Especifica o nome de um certificado.</span><span class="sxs-lookup"><span data-stu-id="57c77-120">Specifies the name of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57c77-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57c77-121">-PassThru</span></span>
<span data-ttu-id="57c77-122">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="57c77-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="57c77-123">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="57c77-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="57c77-124">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="57c77-124">-VaultName</span></span>
<span data-ttu-id="57c77-125">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="57c77-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="57c77-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="57c77-126">-Confirm</span></span>
<span data-ttu-id="57c77-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57c77-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57c77-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57c77-128">-WhatIf</span></span>
<span data-ttu-id="57c77-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="57c77-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57c77-130">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="57c77-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57c77-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="57c77-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57c77-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57c77-132">CommonParameters</span></span>
<span data-ttu-id="57c77-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57c77-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57c77-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57c77-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57c77-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="57c77-135">INPUTS</span></span>

### <span data-ttu-id="57c77-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="57c77-136">None</span></span>
<span data-ttu-id="57c77-137">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="57c77-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="57c77-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="57c77-138">OUTPUTS</span></span>

### <span data-ttu-id="57c77-139">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="57c77-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="57c77-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="57c77-140">NOTES</span></span>

## <span data-ttu-id="57c77-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="57c77-141">RELATED LINKS</span></span>

[<span data-ttu-id="57c77-142">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="57c77-142">Get-AzureKeyVaultCertificateOperation</span></span>](./Get-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="57c77-143">Parar-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="57c77-143">Stop-AzureKeyVaultCertificateOperation</span></span>](./Stop-AzureKeyVaultCertificateOperation.md)

