---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2659C06A-AE5B-4F7B-B9EF-069A74E12560
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateOperation.md
ms.openlocfilehash: d40489471e94474e83243803b5c64cdad1d572d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439940"
---
# <span data-ttu-id="a62ea-101">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="a62ea-101">Remove-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="a62ea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a62ea-102">SYNOPSIS</span></span>
<span data-ttu-id="a62ea-103">Exclui uma operação de certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="a62ea-103">Deletes a certificate operation from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a62ea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a62ea-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a62ea-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a62ea-105">DESCRIPTION</span></span>
<span data-ttu-id="a62ea-106">O cmdlet **Remove-AzureKeyVaultCertificateOperation** exclui uma operação de certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="a62ea-106">The **Remove-AzureKeyVaultCertificateOperation** cmdlet deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="a62ea-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a62ea-107">EXAMPLES</span></span>

### <span data-ttu-id="a62ea-108">Exemplo 1: remover uma operação de certificado</span><span class="sxs-lookup"><span data-stu-id="a62ea-108">Example 1: Remove a certificate operation</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01" -Force
```

<span data-ttu-id="a62ea-109">Esse comando Remove a operação de certificado chamada TestCert01 do cofre da chave ContosoKV01 sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="a62ea-109">This command removes the certificate operation named TestCert01 from the ContosoKV01 key vault without prompting for confirmation.</span></span>

## <span data-ttu-id="a62ea-110">OS</span><span class="sxs-lookup"><span data-stu-id="a62ea-110">PARAMETERS</span></span>

### <span data-ttu-id="a62ea-111">-Force</span><span class="sxs-lookup"><span data-stu-id="a62ea-111">-Force</span></span>
<span data-ttu-id="a62ea-112">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="a62ea-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a62ea-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="a62ea-113">-Name</span></span>
<span data-ttu-id="a62ea-114">Especifica o nome de um certificado.</span><span class="sxs-lookup"><span data-stu-id="a62ea-114">Specifies the name of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a62ea-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a62ea-115">-PassThru</span></span>
<span data-ttu-id="a62ea-116">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="a62ea-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a62ea-117">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="a62ea-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a62ea-118">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="a62ea-118">-VaultName</span></span>
<span data-ttu-id="a62ea-119">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="a62ea-119">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="a62ea-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a62ea-120">-Confirm</span></span>
<span data-ttu-id="a62ea-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a62ea-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a62ea-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a62ea-122">-WhatIf</span></span>
<span data-ttu-id="a62ea-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a62ea-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a62ea-124">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a62ea-124">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a62ea-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a62ea-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a62ea-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a62ea-126">-DefaultProfile</span></span>
<span data-ttu-id="a62ea-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a62ea-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a62ea-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a62ea-128">CommonParameters</span></span>
<span data-ttu-id="a62ea-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a62ea-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a62ea-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a62ea-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a62ea-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a62ea-131">INPUTS</span></span>

## <span data-ttu-id="a62ea-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a62ea-132">OUTPUTS</span></span>

### <span data-ttu-id="a62ea-133">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="a62ea-133">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="a62ea-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a62ea-134">NOTES</span></span>

## <span data-ttu-id="a62ea-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a62ea-135">RELATED LINKS</span></span>

[<span data-ttu-id="a62ea-136">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="a62ea-136">Get-AzureKeyVaultCertificateOperation</span></span>](./Get-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="a62ea-137">Parar-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="a62ea-137">Stop-AzureKeyVaultCertificateOperation</span></span>](./Stop-AzureKeyVaultCertificateOperation.md)

