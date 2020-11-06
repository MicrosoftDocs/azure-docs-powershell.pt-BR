---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificateorganizationdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificateOrganizationDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificateOrganizationDetails.md
ms.openlocfilehash: 7ce93670f6974e51fe634dea3adf81d3800b3a1f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433242"
---
# <span data-ttu-id="c303d-101">New-AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="c303d-101">New-AzureKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="c303d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c303d-102">SYNOPSIS</span></span>
<span data-ttu-id="c303d-103">Cria um objeto de detalhes da organização do certificado na memória.</span><span class="sxs-lookup"><span data-stu-id="c303d-103">Creates an in-memory certificate organization details object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c303d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c303d-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificateOrganizationDetails [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c303d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c303d-105">DESCRIPTION</span></span>
<span data-ttu-id="c303d-106">O cmdlet **New-AzureKeyVaultCertificateOrganizationDetails** cria um objeto de detalhes da organização do certificado na memória.</span><span class="sxs-lookup"><span data-stu-id="c303d-106">The **New-AzureKeyVaultCertificateOrganizationDetails** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="c303d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c303d-107">EXAMPLES</span></span>

### <span data-ttu-id="c303d-108">Exemplo 1: criar um objeto de detalhes da organização</span><span class="sxs-lookup"><span data-stu-id="c303d-108">Example 1: Create an organization details object</span></span>
```powershell
PS C:\> $AdminDetails = New-AzureKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
PS C:\> New-AzureKeyVaultCertificateOrganizationDetails -AdministratorDetails $AdminDetails

Id AdministratorDetails
-- --------------------
   {Patti}
```

<span data-ttu-id="c303d-109">O primeiro comando cria um objeto de detalhes do administrador do certificado e, em seguida, armazena-o na variável $AdminDetails.</span><span class="sxs-lookup"><span data-stu-id="c303d-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>
<span data-ttu-id="c303d-110">O segundo comando cria um objeto de detalhes da organização do certificado e, em seguida, armazena-o na variável $OrgDetails.</span><span class="sxs-lookup"><span data-stu-id="c303d-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="c303d-111">OS</span><span class="sxs-lookup"><span data-stu-id="c303d-111">PARAMETERS</span></span>

### <span data-ttu-id="c303d-112">-AdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="c303d-112">-AdministratorDetails</span></span>
<span data-ttu-id="c303d-113">Especifica os administradores de organização do certificado.</span><span class="sxs-lookup"><span data-stu-id="c303d-113">Specifies the certificate organization administrators.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c303d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c303d-114">-DefaultProfile</span></span>
<span data-ttu-id="c303d-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c303d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c303d-116">-ID</span><span class="sxs-lookup"><span data-stu-id="c303d-116">-Id</span></span>
<span data-ttu-id="c303d-117">Especifica o identificador para a organização.</span><span class="sxs-lookup"><span data-stu-id="c303d-117">Specifies the identifier for the organization.</span></span>

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

### <span data-ttu-id="c303d-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c303d-118">-Confirm</span></span>
<span data-ttu-id="c303d-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c303d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c303d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c303d-120">-WhatIf</span></span>
<span data-ttu-id="c303d-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c303d-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c303d-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c303d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c303d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c303d-123">CommonParameters</span></span>
<span data-ttu-id="c303d-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c303d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c303d-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c303d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c303d-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c303d-126">INPUTS</span></span>

### <span data-ttu-id="c303d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c303d-127">System.String</span></span>

### <span data-ttu-id="c303d-128">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateAdministratorDetails, Microsoft. Azure. Commands. keyvault, Version = 5.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c303d-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails, Microsoft.Azure.Commands.KeyVault, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c303d-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c303d-129">OUTPUTS</span></span>

### <span data-ttu-id="c303d-130">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="c303d-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="c303d-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c303d-131">NOTES</span></span>

## <span data-ttu-id="c303d-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c303d-132">RELATED LINKS</span></span>

[<span data-ttu-id="c303d-133">New-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="c303d-133">New-AzureKeyVaultCertificateAdministratorDetails</span></span>](./New-AzureKeyVaultCertificateAdministratorDetails.md)
