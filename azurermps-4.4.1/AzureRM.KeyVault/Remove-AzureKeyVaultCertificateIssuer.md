---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 3ef23bcbddc1f8a5c5c235c72dac32f535a71a29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439941"
---
# <span data-ttu-id="94a97-101">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="94a97-101">Remove-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="94a97-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="94a97-102">SYNOPSIS</span></span>
<span data-ttu-id="94a97-103">Exclui um emissor de certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="94a97-103">Deletes a certificate issuer from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94a97-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="94a97-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94a97-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="94a97-105">DESCRIPTION</span></span>
<span data-ttu-id="94a97-106">O cmdlet **Remove-AzureKeyVaultCertificateIssuer** exclui um emissor de certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="94a97-106">The **Remove-AzureKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="94a97-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="94a97-107">EXAMPLES</span></span>

### <span data-ttu-id="94a97-108">Exemplo 1: remover um emissor de certificado</span><span class="sxs-lookup"><span data-stu-id="94a97-108">Example 1: Remove a certificate issuer</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force
```

<span data-ttu-id="94a97-109">Esse comando Remove o emissor do certificado chamado TestIssuer01 do cofre da chave ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="94a97-109">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="94a97-110">OS</span><span class="sxs-lookup"><span data-stu-id="94a97-110">PARAMETERS</span></span>

### <span data-ttu-id="94a97-111">-Force</span><span class="sxs-lookup"><span data-stu-id="94a97-111">-Force</span></span>
<span data-ttu-id="94a97-112">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="94a97-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="94a97-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="94a97-113">-Name</span></span>
<span data-ttu-id="94a97-114">Especifica o nome do emissor que será removido.</span><span class="sxs-lookup"><span data-stu-id="94a97-114">Specifies the name of the issuer to remove.</span></span>

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

### <span data-ttu-id="94a97-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94a97-115">-PassThru</span></span>
<span data-ttu-id="94a97-116">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="94a97-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="94a97-117">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="94a97-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="94a97-118">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="94a97-118">-VaultName</span></span>
<span data-ttu-id="94a97-119">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="94a97-119">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="94a97-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="94a97-120">-Confirm</span></span>
<span data-ttu-id="94a97-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94a97-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94a97-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94a97-122">-WhatIf</span></span>
<span data-ttu-id="94a97-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="94a97-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94a97-124">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="94a97-124">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94a97-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="94a97-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94a97-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94a97-126">-DefaultProfile</span></span>
<span data-ttu-id="94a97-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="94a97-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94a97-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94a97-128">CommonParameters</span></span>
<span data-ttu-id="94a97-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94a97-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94a97-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94a97-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94a97-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="94a97-131">INPUTS</span></span>

## <span data-ttu-id="94a97-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="94a97-132">OUTPUTS</span></span>

### <span data-ttu-id="94a97-133">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="94a97-133">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="94a97-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="94a97-134">NOTES</span></span>

## <span data-ttu-id="94a97-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="94a97-135">RELATED LINKS</span></span>

[<span data-ttu-id="94a97-136">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="94a97-136">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="94a97-137">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="94a97-137">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


