---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificate
schema: 2.0.0
ms.openlocfilehash: 662304cff991da0d9ffe9d946e63bc94ba51e4a9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785225"
---
# <span data-ttu-id="4eace-101">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="4eace-101">Remove-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="4eace-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4eace-102">SYNOPSIS</span></span>
<span data-ttu-id="4eace-103">Remove um certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="4eace-103">Removes a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4eace-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4eace-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Force] [-InRemovedState] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4eace-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4eace-105">DESCRIPTION</span></span>
<span data-ttu-id="4eace-106">O cmdlet **Remove-AzureKeyVaultCertificate** remove um certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="4eace-106">The **Remove-AzureKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="4eace-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4eace-107">EXAMPLES</span></span>

### <span data-ttu-id="4eace-108">Exemplo 1: remover um certificado</span><span class="sxs-lookup"><span data-stu-id="4eace-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "SelfSigned01" -PassThru -Force
Name        : selfSigned01
Certificate : 
Thumbprint  : 
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:29:33 PM
Updated     : 2/8/2016 11:29:33 PM
```

<span data-ttu-id="4eace-109">Esse comando Remove o certificado chamado SelfSigned01 do cofre de chaves chamado ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="4eace-109">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="4eace-110">Esse comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="4eace-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="4eace-111">Portanto, o cmdlet não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="4eace-111">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="4eace-112">Exemplo 3: limpar o certificado excluído do cofre de chaves permanentemente</span><span class="sxs-lookup"><span data-stu-id="4eace-112">Example 3: Purge the deleted certificate from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="4eace-113">Esse comando remove permanentemente o certificado chamado ' MyCert ' do cofre de chaves chamado ' contoso '.</span><span class="sxs-lookup"><span data-stu-id="4eace-113">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="4eace-114">A execução deste cmdlet requer a permissão ' limpar ', que deve ter sido concedida anteriormente e explicitamente ao usuário neste cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="4eace-114">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="4eace-115">OS</span><span class="sxs-lookup"><span data-stu-id="4eace-115">PARAMETERS</span></span>

### <span data-ttu-id="4eace-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eace-116">-DefaultProfile</span></span>
<span data-ttu-id="4eace-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4eace-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4eace-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4eace-118">-Force</span></span>
<span data-ttu-id="4eace-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="4eace-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4eace-120">-Inremovestate</span><span class="sxs-lookup"><span data-stu-id="4eace-120">-InRemovedState</span></span>
<span data-ttu-id="4eace-121">Se presente, remove permanentemente o certificado excluído anteriormente</span><span class="sxs-lookup"><span data-stu-id="4eace-121">If present, removes the previously deleted certificate permanently</span></span>

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

### <span data-ttu-id="4eace-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="4eace-122">-Name</span></span>
<span data-ttu-id="4eace-123">Especifica o nome do certificado que este cmdlet Remove de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="4eace-123">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="4eace-124">Esse cmdlet constrói o nome de domínio totalmente qualificado (FQDN) de um certificado com base no nome que esse parâmetro especifica, o nome do cofre de chaves e o ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="4eace-124">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4eace-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4eace-125">-PassThru</span></span>
<span data-ttu-id="4eace-126">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="4eace-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4eace-127">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="4eace-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4eace-128">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="4eace-128">-VaultName</span></span>
<span data-ttu-id="4eace-129">Especifica o nome do cofre de chaves do qual esse cmdlet Remove um certificado.</span><span class="sxs-lookup"><span data-stu-id="4eace-129">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="4eace-130">Esse cmdlet constrói o FQDN de um cofre de chaves com base no nome especificado pelo parâmetro e no seu ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="4eace-130">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="4eace-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4eace-131">-Confirm</span></span>
<span data-ttu-id="4eace-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4eace-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4eace-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4eace-133">-WhatIf</span></span>
<span data-ttu-id="4eace-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4eace-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4eace-135">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4eace-135">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4eace-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4eace-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4eace-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eace-137">CommonParameters</span></span>
<span data-ttu-id="4eace-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4eace-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eace-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4eace-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eace-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4eace-140">INPUTS</span></span>

## <span data-ttu-id="4eace-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4eace-141">OUTPUTS</span></span>

### <span data-ttu-id="4eace-142">Microsoft. Azure. Commands. keyvault. Models. CertificateBundle</span><span class="sxs-lookup"><span data-stu-id="4eace-142">Microsoft.Azure.Commands.KeyVault.Models.CertificateBundle</span></span>

## <span data-ttu-id="4eace-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4eace-143">NOTES</span></span>

## <span data-ttu-id="4eace-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4eace-144">RELATED LINKS</span></span>

[<span data-ttu-id="4eace-145">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="4eace-145">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="4eace-146">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="4eace-146">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)

[<span data-ttu-id="4eace-147">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="4eace-147">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="4eace-148">Desfazer-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="4eace-148">Undo-AzureKeyVaultCertificateRemoval</span></span>](./Undo-AzureKeyVaultCertificateRemoval.md)
