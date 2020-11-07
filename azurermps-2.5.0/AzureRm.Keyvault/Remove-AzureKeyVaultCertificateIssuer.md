---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificateissuer
schema: 2.0.0
ms.openlocfilehash: 4c732cdfc175c47e9bd8125234cb1d33f1b19097
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785217"
---
# <span data-ttu-id="c2673-101">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="c2673-101">Remove-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="c2673-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c2673-102">SYNOPSIS</span></span>
<span data-ttu-id="c2673-103">Exclui um emissor de certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="c2673-103">Deletes a certificate issuer from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2673-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c2673-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2673-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c2673-105">DESCRIPTION</span></span>
<span data-ttu-id="c2673-106">O cmdlet **Remove-AzureKeyVaultCertificateIssuer** exclui um emissor de certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="c2673-106">The **Remove-AzureKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="c2673-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c2673-107">EXAMPLES</span></span>

### <span data-ttu-id="c2673-108">Exemplo 1: remover um emissor de certificado</span><span class="sxs-lookup"><span data-stu-id="c2673-108">Example 1: Remove a certificate issuer</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force
```

<span data-ttu-id="c2673-109">Esse comando Remove o emissor do certificado chamado TestIssuer01 do cofre da chave ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="c2673-109">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="c2673-110">OS</span><span class="sxs-lookup"><span data-stu-id="c2673-110">PARAMETERS</span></span>

### <span data-ttu-id="c2673-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2673-111">-DefaultProfile</span></span>
<span data-ttu-id="c2673-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c2673-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2673-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c2673-113">-Force</span></span>
<span data-ttu-id="c2673-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="c2673-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c2673-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="c2673-115">-Name</span></span>
<span data-ttu-id="c2673-116">Especifica o nome do emissor que será removido.</span><span class="sxs-lookup"><span data-stu-id="c2673-116">Specifies the name of the issuer to remove.</span></span>

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

### <span data-ttu-id="c2673-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2673-117">-PassThru</span></span>
<span data-ttu-id="c2673-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="c2673-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c2673-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="c2673-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c2673-120">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="c2673-120">-VaultName</span></span>
<span data-ttu-id="c2673-121">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="c2673-121">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="c2673-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c2673-122">-Confirm</span></span>
<span data-ttu-id="c2673-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2673-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2673-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2673-124">-WhatIf</span></span>
<span data-ttu-id="c2673-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c2673-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2673-126">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c2673-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2673-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c2673-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2673-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2673-128">CommonParameters</span></span>
<span data-ttu-id="c2673-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2673-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2673-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2673-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2673-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c2673-131">INPUTS</span></span>

## <span data-ttu-id="c2673-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c2673-132">OUTPUTS</span></span>

### <span data-ttu-id="c2673-133">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="c2673-133">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="c2673-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c2673-134">NOTES</span></span>

## <span data-ttu-id="c2673-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c2673-135">RELATED LINKS</span></span>

[<span data-ttu-id="c2673-136">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="c2673-136">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="c2673-137">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="c2673-137">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


