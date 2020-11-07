---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificateadministratordetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
ms.openlocfilehash: 39deb08468912bf727198ec4f90f5f4f0680941f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940684"
---
# <span data-ttu-id="cae57-101">New-AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="cae57-101">New-AzKeyVaultCertificateAdministratorDetail</span></span>

## <span data-ttu-id="cae57-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cae57-102">SYNOPSIS</span></span>
<span data-ttu-id="cae57-103">Cria um objeto de detalhes do administrador do certificado na memória.</span><span class="sxs-lookup"><span data-stu-id="cae57-103">Creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="cae57-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cae57-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateAdministratorDetail [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cae57-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cae57-105">DESCRIPTION</span></span>
<span data-ttu-id="cae57-106">O cmdlet **New-AzKeyVaultCertificateAdministratorDetail** cria um objeto de detalhes do administrador do certificado na memória.</span><span class="sxs-lookup"><span data-stu-id="cae57-106">The **New-AzKeyVaultCertificateAdministratorDetail** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="cae57-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cae57-107">EXAMPLES</span></span>

### <span data-ttu-id="cae57-108">Exemplo 1: criar um objeto de detalhes do administrador do certificado</span><span class="sxs-lookup"><span data-stu-id="cae57-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
PS C:\> $AdminDetails

FirstName LastName EmailAddress             PhoneNumber
--------- -------- ------------             -----------
Patti     Fuller   patti.fuller@contoso.com 5553334444
```

<span data-ttu-id="cae57-109">Esse comando cria um objeto de detalhes do administrador do certificado na memória e, em seguida, armazena-o na variável $AdminDetails.</span><span class="sxs-lookup"><span data-stu-id="cae57-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="cae57-110">OS</span><span class="sxs-lookup"><span data-stu-id="cae57-110">PARAMETERS</span></span>

### <span data-ttu-id="cae57-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cae57-111">-DefaultProfile</span></span>
<span data-ttu-id="cae57-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="cae57-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cae57-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="cae57-113">-EmailAddress</span></span>
<span data-ttu-id="cae57-114">Especifica o endereço de email do administrador do certificado.</span><span class="sxs-lookup"><span data-stu-id="cae57-114">Specifies the email address for the certificate administrator.</span></span>

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

### <span data-ttu-id="cae57-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="cae57-115">-FirstName</span></span>
<span data-ttu-id="cae57-116">Especifica o primeiro nome do administrador do certificado.</span><span class="sxs-lookup"><span data-stu-id="cae57-116">Specifies the first name of the certificate administrator.</span></span>

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

### <span data-ttu-id="cae57-117">-LastName</span><span class="sxs-lookup"><span data-stu-id="cae57-117">-LastName</span></span>
<span data-ttu-id="cae57-118">Especifica o último nome do administrador do certificado.</span><span class="sxs-lookup"><span data-stu-id="cae57-118">Specifies the last name of the certificate administrator.</span></span>

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

### <span data-ttu-id="cae57-119">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="cae57-119">-PhoneNumber</span></span>
<span data-ttu-id="cae57-120">Especifica o número de telefone do administrador do certificado.</span><span class="sxs-lookup"><span data-stu-id="cae57-120">Specifies the phone number of the certificate administrator.</span></span>

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

### <span data-ttu-id="cae57-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cae57-121">-Confirm</span></span>
<span data-ttu-id="cae57-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cae57-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cae57-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cae57-123">-WhatIf</span></span>
<span data-ttu-id="cae57-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cae57-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cae57-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cae57-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cae57-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cae57-126">CommonParameters</span></span>
<span data-ttu-id="cae57-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cae57-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cae57-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cae57-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cae57-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cae57-129">INPUTS</span></span>

### <span data-ttu-id="cae57-130">System. String</span><span class="sxs-lookup"><span data-stu-id="cae57-130">System.String</span></span>

## <span data-ttu-id="cae57-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cae57-131">OUTPUTS</span></span>

### <span data-ttu-id="cae57-132">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="cae57-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="cae57-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cae57-133">NOTES</span></span>

## <span data-ttu-id="cae57-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cae57-134">RELATED LINKS</span></span>

[<span data-ttu-id="cae57-135">New-AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="cae57-135">New-AzKeyVaultCertificateOrganizationDetail</span></span>](./New-AzKeyVaultCertificateOrganizationDetail.md)

