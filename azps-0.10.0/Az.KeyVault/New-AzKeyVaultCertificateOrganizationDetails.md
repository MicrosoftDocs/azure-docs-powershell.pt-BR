---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/new-AzKeyvaultcertificateorganizationdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetails.md
ms.openlocfilehash: 76208f8d4c1b8b1b463ea5a0f24a4e34e7a82855
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776665"
---
# <span data-ttu-id="f6659-101">New-AzKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="f6659-101">New-AzKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="f6659-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f6659-102">SYNOPSIS</span></span>
<span data-ttu-id="f6659-103">Cria um objeto de detalhes da organização do certificado na memória.</span><span class="sxs-lookup"><span data-stu-id="f6659-103">Creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="f6659-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f6659-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateOrganizationDetails [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6659-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f6659-105">DESCRIPTION</span></span>
<span data-ttu-id="f6659-106">O cmdlet **New-AzKeyVaultCertificateOrganizationDetails** cria um objeto de detalhes da organização do certificado na memória.</span><span class="sxs-lookup"><span data-stu-id="f6659-106">The **New-AzKeyVaultCertificateOrganizationDetails** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="f6659-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f6659-107">EXAMPLES</span></span>

### <span data-ttu-id="f6659-108">Exemplo 1: criar um objeto de detalhes da organização</span><span class="sxs-lookup"><span data-stu-id="f6659-108">Example 1: Create an organization details object</span></span>
```
PS C:\>$AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
$OrgDetails = New-AzKeyVaultCertificateOrganizationDetails -Name "Contoso" -Address1 "1 Redmond Way" -Address2 "Suite 906" -City "Redmond" -State "WA" -Zip 98052 -Country "US" -AdministratorDetails $AdminDetails
```

<span data-ttu-id="f6659-109">O primeiro comando cria um objeto de detalhes do administrador do certificado e, em seguida, armazena-o na variável $AdminDetails.</span><span class="sxs-lookup"><span data-stu-id="f6659-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

<span data-ttu-id="f6659-110">O segundo comando cria um objeto de detalhes da organização do certificado e, em seguida, armazena-o na variável $OrgDetails.</span><span class="sxs-lookup"><span data-stu-id="f6659-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="f6659-111">OS</span><span class="sxs-lookup"><span data-stu-id="f6659-111">PARAMETERS</span></span>

### <span data-ttu-id="f6659-112">-AdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="f6659-112">-AdministratorDetails</span></span>
<span data-ttu-id="f6659-113">Especifica os administradores de organização do certificado.</span><span class="sxs-lookup"><span data-stu-id="f6659-113">Specifies the certificate organization administrators.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6659-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6659-114">-DefaultProfile</span></span>
<span data-ttu-id="f6659-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f6659-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6659-116">-ID</span><span class="sxs-lookup"><span data-stu-id="f6659-116">-Id</span></span>
<span data-ttu-id="f6659-117">Especifica o identificador para a organização.</span><span class="sxs-lookup"><span data-stu-id="f6659-117">Specifies the identifier for the organization.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6659-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f6659-118">-Confirm</span></span>
<span data-ttu-id="f6659-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6659-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6659-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6659-120">-WhatIf</span></span>
<span data-ttu-id="f6659-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f6659-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6659-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f6659-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6659-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6659-123">CommonParameters</span></span>
<span data-ttu-id="f6659-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6659-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6659-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6659-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6659-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f6659-126">INPUTS</span></span>

### <span data-ttu-id="f6659-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f6659-127">None</span></span>
<span data-ttu-id="f6659-128">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="f6659-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f6659-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f6659-129">OUTPUTS</span></span>

### <span data-ttu-id="f6659-130">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="f6659-130">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="f6659-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f6659-131">NOTES</span></span>

## <span data-ttu-id="f6659-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f6659-132">RELATED LINKS</span></span>

[<span data-ttu-id="f6659-133">New-AzKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="f6659-133">New-AzKeyVaultCertificateAdministratorDetails</span></span>](./New-AzKeyVaultCertificateAdministratorDetails.md)

