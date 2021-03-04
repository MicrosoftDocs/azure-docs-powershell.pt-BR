---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/powershell/module/az.keyvault/new-azkeyvaultcertificateadministratordetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
ms.openlocfilehash: e72729b1721fb31ca2ce3a52d33f0295c55bb537
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891823"
---
# <span data-ttu-id="3c31c-101">New-AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="3c31c-101">New-AzKeyVaultCertificateAdministratorDetail</span></span>

## <span data-ttu-id="3c31c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c31c-102">SYNOPSIS</span></span>
<span data-ttu-id="3c31c-103">Cria um objeto de detalhes de administrador de certificado na memória.</span><span class="sxs-lookup"><span data-stu-id="3c31c-103">Creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="3c31c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3c31c-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateAdministratorDetail [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c31c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3c31c-105">DESCRIPTION</span></span>
<span data-ttu-id="3c31c-106">O cmdlet **New-AzKeyVaultCertificateAdministratorDetail** cria um objeto de detalhes de administrador de certificado na memória.</span><span class="sxs-lookup"><span data-stu-id="3c31c-106">The **New-AzKeyVaultCertificateAdministratorDetail** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="3c31c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3c31c-107">EXAMPLES</span></span>

### <span data-ttu-id="3c31c-108">Exemplo 1: Criar um objeto de detalhes do administrador de certificados</span><span class="sxs-lookup"><span data-stu-id="3c31c-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
PS C:\> $AdminDetails

FirstName LastName EmailAddress             PhoneNumber
--------- -------- ------------             -----------
Patti     Fuller   patti.fuller@contoso.com 5553334444
```

<span data-ttu-id="3c31c-109">Esse comando cria um objeto de detalhes de administrador de certificado na memória e o armazena na variável $AdminDetails de memória.</span><span class="sxs-lookup"><span data-stu-id="3c31c-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="3c31c-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3c31c-110">PARAMETERS</span></span>

### <span data-ttu-id="3c31c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c31c-111">-DefaultProfile</span></span>
<span data-ttu-id="3c31c-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="3c31c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c31c-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="3c31c-113">-EmailAddress</span></span>
<span data-ttu-id="3c31c-114">Especifica o endereço de email do administrador do certificado.</span><span class="sxs-lookup"><span data-stu-id="3c31c-114">Specifies the email address for the certificate administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c31c-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="3c31c-115">-FirstName</span></span>
<span data-ttu-id="3c31c-116">Especifica o primeiro nome do administrador do certificado.</span><span class="sxs-lookup"><span data-stu-id="3c31c-116">Specifies the first name of the certificate administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c31c-117">-LastName</span><span class="sxs-lookup"><span data-stu-id="3c31c-117">-LastName</span></span>
<span data-ttu-id="3c31c-118">Especifica o sobrenome do administrador do certificado.</span><span class="sxs-lookup"><span data-stu-id="3c31c-118">Specifies the last name of the certificate administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c31c-119">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="3c31c-119">-PhoneNumber</span></span>
<span data-ttu-id="3c31c-120">Especifica o número de telefone do administrador do certificado.</span><span class="sxs-lookup"><span data-stu-id="3c31c-120">Specifies the phone number of the certificate administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c31c-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c31c-121">-Confirm</span></span>
<span data-ttu-id="3c31c-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c31c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c31c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c31c-123">-WhatIf</span></span>
<span data-ttu-id="3c31c-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3c31c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c31c-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3c31c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c31c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c31c-126">CommonParameters</span></span>
<span data-ttu-id="3c31c-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c31c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c31c-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c31c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c31c-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3c31c-129">INPUTS</span></span>

### <span data-ttu-id="3c31c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="3c31c-130">System.String</span></span>

## <span data-ttu-id="3c31c-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3c31c-131">OUTPUTS</span></span>

### <span data-ttu-id="3c31c-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="3c31c-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="3c31c-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="3c31c-133">NOTES</span></span>

## <span data-ttu-id="3c31c-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3c31c-134">RELATED LINKS</span></span>

[<span data-ttu-id="3c31c-135">New-AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="3c31c-135">New-AzKeyVaultCertificateOrganizationDetail</span></span>](./New-AzKeyVaultCertificateOrganizationDetail.md)

