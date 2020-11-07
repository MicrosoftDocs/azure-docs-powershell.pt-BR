---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 204ee5a7a4d0e5247ae3de239dce650deb4cff0c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775780"
---
# <span data-ttu-id="12f52-101">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="12f52-101">Remove-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="12f52-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="12f52-102">SYNOPSIS</span></span>
<span data-ttu-id="12f52-103">Exclui um emissor de certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="12f52-103">Deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="12f52-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12f52-104">SYNTAX</span></span>

```
Remove-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12f52-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="12f52-105">DESCRIPTION</span></span>
<span data-ttu-id="12f52-106">O cmdlet **Remove-AzKeyVaultCertificateIssuer** exclui um emissor de certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="12f52-106">The **Remove-AzKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="12f52-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12f52-107">EXAMPLES</span></span>

### <span data-ttu-id="12f52-108">Exemplo 1: remover um emissor de certificado</span><span class="sxs-lookup"><span data-stu-id="12f52-108">Example 1: Remove a certificate issuer</span></span>
```
PS C:\>Remove-AzKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force
```

<span data-ttu-id="12f52-109">Esse comando Remove o emissor do certificado chamado TestIssuer01 do cofre da chave ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="12f52-109">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="12f52-110">OS</span><span class="sxs-lookup"><span data-stu-id="12f52-110">PARAMETERS</span></span>

### <span data-ttu-id="12f52-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12f52-111">-DefaultProfile</span></span>
<span data-ttu-id="12f52-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="12f52-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12f52-113">-Force</span><span class="sxs-lookup"><span data-stu-id="12f52-113">-Force</span></span>
<span data-ttu-id="12f52-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="12f52-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="12f52-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="12f52-115">-Name</span></span>
<span data-ttu-id="12f52-116">Especifica o nome do emissor que será removido.</span><span class="sxs-lookup"><span data-stu-id="12f52-116">Specifies the name of the issuer to remove.</span></span>

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

### <span data-ttu-id="12f52-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12f52-117">-PassThru</span></span>
<span data-ttu-id="12f52-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="12f52-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="12f52-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="12f52-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="12f52-120">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="12f52-120">-VaultName</span></span>
<span data-ttu-id="12f52-121">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="12f52-121">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="12f52-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="12f52-122">-Confirm</span></span>
<span data-ttu-id="12f52-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12f52-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12f52-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12f52-124">-WhatIf</span></span>
<span data-ttu-id="12f52-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="12f52-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12f52-126">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="12f52-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12f52-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="12f52-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12f52-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12f52-128">CommonParameters</span></span>
<span data-ttu-id="12f52-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12f52-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12f52-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12f52-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12f52-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="12f52-131">INPUTS</span></span>

### <span data-ttu-id="12f52-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="12f52-132">None</span></span>
<span data-ttu-id="12f52-133">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="12f52-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="12f52-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="12f52-134">OUTPUTS</span></span>

### <span data-ttu-id="12f52-135">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="12f52-135">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="12f52-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="12f52-136">NOTES</span></span>

## <span data-ttu-id="12f52-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12f52-137">RELATED LINKS</span></span>

[<span data-ttu-id="12f52-138">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="12f52-138">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="12f52-139">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="12f52-139">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


