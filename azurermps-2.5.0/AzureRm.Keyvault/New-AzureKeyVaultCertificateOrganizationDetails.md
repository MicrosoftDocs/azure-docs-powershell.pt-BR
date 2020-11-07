---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificateorganizationdetails
schema: 2.0.0
ms.openlocfilehash: 76e0d37ac38c8b9799093ff3a4f4ea10c2fce2f4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786101"
---
# <span data-ttu-id="bdaed-101">New-AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="bdaed-101">New-AzureKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="bdaed-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bdaed-102">SYNOPSIS</span></span>
<span data-ttu-id="bdaed-103">Cria um objeto de detalhes da organização do certificado na memória.</span><span class="sxs-lookup"><span data-stu-id="bdaed-103">Creates an in-memory certificate organization details object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdaed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bdaed-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificateOrganizationDetails [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdaed-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bdaed-105">DESCRIPTION</span></span>
<span data-ttu-id="bdaed-106">O cmdlet **New-AzureKeyVaultCertificateOrganizationDetails** cria um objeto de detalhes da organização do certificado na memória.</span><span class="sxs-lookup"><span data-stu-id="bdaed-106">The **New-AzureKeyVaultCertificateOrganizationDetails** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="bdaed-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bdaed-107">EXAMPLES</span></span>

### <span data-ttu-id="bdaed-108">Exemplo 1: criar um objeto de detalhes da organização</span><span class="sxs-lookup"><span data-stu-id="bdaed-108">Example 1: Create an organization details object</span></span>
```
PS C:\>$AdminDetails = New-AzureKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
$OrgDetails = New-AzureKeyVaultCertificateOrganizationDetails -Name "Contoso" -Address1 "1 Redmond Way" -Address2 "Suite 906" -City "Redmond" -State "WA" -Zip 98052 -Country "US" -AdministratorDetails $AdminDetails
```

<span data-ttu-id="bdaed-109">O primeiro comando cria um objeto de detalhes do administrador do certificado e, em seguida, armazena-o na variável $AdminDetails.</span><span class="sxs-lookup"><span data-stu-id="bdaed-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

<span data-ttu-id="bdaed-110">O segundo comando cria um objeto de detalhes da organização do certificado e, em seguida, armazena-o na variável $OrgDetails.</span><span class="sxs-lookup"><span data-stu-id="bdaed-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="bdaed-111">OS</span><span class="sxs-lookup"><span data-stu-id="bdaed-111">PARAMETERS</span></span>

### <span data-ttu-id="bdaed-112">-AdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="bdaed-112">-AdministratorDetails</span></span>
<span data-ttu-id="bdaed-113">Especifica os administradores de organização do certificado.</span><span class="sxs-lookup"><span data-stu-id="bdaed-113">Specifies the certificate organization administrators.</span></span>

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

### <span data-ttu-id="bdaed-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdaed-114">-DefaultProfile</span></span>
<span data-ttu-id="bdaed-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="bdaed-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bdaed-116">-ID</span><span class="sxs-lookup"><span data-stu-id="bdaed-116">-Id</span></span>
<span data-ttu-id="bdaed-117">Especifica o identificador para a organização.</span><span class="sxs-lookup"><span data-stu-id="bdaed-117">Specifies the identifier for the organization.</span></span>

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

### <span data-ttu-id="bdaed-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bdaed-118">-Confirm</span></span>
<span data-ttu-id="bdaed-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdaed-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdaed-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdaed-120">-WhatIf</span></span>
<span data-ttu-id="bdaed-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bdaed-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdaed-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bdaed-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdaed-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdaed-123">CommonParameters</span></span>
<span data-ttu-id="bdaed-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdaed-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdaed-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdaed-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdaed-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bdaed-126">INPUTS</span></span>

## <span data-ttu-id="bdaed-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bdaed-127">OUTPUTS</span></span>

### <span data-ttu-id="bdaed-128">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="bdaed-128">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="bdaed-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bdaed-129">NOTES</span></span>

## <span data-ttu-id="bdaed-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bdaed-130">RELATED LINKS</span></span>

[<span data-ttu-id="bdaed-131">New-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="bdaed-131">New-AzureKeyVaultCertificateAdministratorDetails</span></span>](./New-AzureKeyVaultCertificateAdministratorDetails.md)

