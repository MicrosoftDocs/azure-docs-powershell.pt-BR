---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2659C06A-AE5B-4F7B-B9EF-069A74E12560
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateOperation.md
ms.openlocfilehash: 37cc2025b97e16a2af313a2f4dd2cf7dfe815b7b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775777"
---
# <span data-ttu-id="a57a6-101">Remove-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="a57a6-101">Remove-AzKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="a57a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a57a6-102">SYNOPSIS</span></span>
<span data-ttu-id="a57a6-103">Exclui uma operação de certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="a57a6-103">Deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="a57a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a57a6-104">SYNTAX</span></span>

```
Remove-AzKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a57a6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a57a6-105">DESCRIPTION</span></span>
<span data-ttu-id="a57a6-106">O cmdlet **Remove-AzKeyVaultCertificateOperation** exclui uma operação de certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="a57a6-106">The **Remove-AzKeyVaultCertificateOperation** cmdlet deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="a57a6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a57a6-107">EXAMPLES</span></span>

### <span data-ttu-id="a57a6-108">Exemplo 1: remover uma operação de certificado</span><span class="sxs-lookup"><span data-stu-id="a57a6-108">Example 1: Remove a certificate operation</span></span>
```
PS C:\>Remove-AzKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01" -Force
```

<span data-ttu-id="a57a6-109">Esse comando Remove a operação de certificado chamada TestCert01 do cofre da chave ContosoKV01 sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="a57a6-109">This command removes the certificate operation named TestCert01 from the ContosoKV01 key vault without prompting for confirmation.</span></span>

## <span data-ttu-id="a57a6-110">OS</span><span class="sxs-lookup"><span data-stu-id="a57a6-110">PARAMETERS</span></span>

### <span data-ttu-id="a57a6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a57a6-111">-DefaultProfile</span></span>
<span data-ttu-id="a57a6-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a57a6-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a57a6-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a57a6-113">-Force</span></span>
<span data-ttu-id="a57a6-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="a57a6-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a57a6-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a57a6-115">-Name</span></span>
<span data-ttu-id="a57a6-116">Especifica o nome de um certificado.</span><span class="sxs-lookup"><span data-stu-id="a57a6-116">Specifies the name of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a57a6-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a57a6-117">-PassThru</span></span>
<span data-ttu-id="a57a6-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="a57a6-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a57a6-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="a57a6-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a57a6-120">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="a57a6-120">-VaultName</span></span>
<span data-ttu-id="a57a6-121">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="a57a6-121">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="a57a6-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a57a6-122">-Confirm</span></span>
<span data-ttu-id="a57a6-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a57a6-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a57a6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a57a6-124">-WhatIf</span></span>
<span data-ttu-id="a57a6-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a57a6-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a57a6-126">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a57a6-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a57a6-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a57a6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a57a6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a57a6-128">CommonParameters</span></span>
<span data-ttu-id="a57a6-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a57a6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a57a6-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a57a6-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a57a6-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a57a6-131">INPUTS</span></span>

### <span data-ttu-id="a57a6-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a57a6-132">None</span></span>
<span data-ttu-id="a57a6-133">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="a57a6-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a57a6-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a57a6-134">OUTPUTS</span></span>

### <span data-ttu-id="a57a6-135">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="a57a6-135">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="a57a6-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a57a6-136">NOTES</span></span>

## <span data-ttu-id="a57a6-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a57a6-137">RELATED LINKS</span></span>

[<span data-ttu-id="a57a6-138">Get-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="a57a6-138">Get-AzKeyVaultCertificateOperation</span></span>](./Get-AzKeyVaultCertificateOperation.md)

[<span data-ttu-id="a57a6-139">Parar-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="a57a6-139">Stop-AzKeyVaultCertificateOperation</span></span>](./Stop-AzKeyVaultCertificateOperation.md)

