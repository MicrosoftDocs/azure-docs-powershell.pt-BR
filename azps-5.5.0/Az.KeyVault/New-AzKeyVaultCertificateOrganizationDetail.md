---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificateorganizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetail.md
ms.openlocfilehash: 56b956aa8a65c4586859325f110f3ce593b2289c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116719"
---
# <span data-ttu-id="3e7bb-101">New-AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="3e7bb-101">New-AzKeyVaultCertificateOrganizationDetail</span></span>

## <span data-ttu-id="3e7bb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3e7bb-102">SYNOPSIS</span></span>
<span data-ttu-id="3e7bb-103">Cria um objeto de detalhes da organização de certificados na memória.</span><span class="sxs-lookup"><span data-stu-id="3e7bb-103">Creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="3e7bb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e7bb-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateOrganizationDetail [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e7bb-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="3e7bb-105">DESCRIPTION</span></span>
<span data-ttu-id="3e7bb-106">O **cmdlet New-AzKeyVaultCertificateOrganizationDetail** cria um objeto de detalhes da organização de certificados de memória.</span><span class="sxs-lookup"><span data-stu-id="3e7bb-106">The **New-AzKeyVaultCertificateOrganizationDetail** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="3e7bb-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3e7bb-107">EXAMPLES</span></span>

### <span data-ttu-id="3e7bb-108">Exemplo 1: Criar um objeto de detalhes da organização</span><span class="sxs-lookup"><span data-stu-id="3e7bb-108">Example 1: Create an organization details object</span></span>
```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails

Id AdministratorDetails
-- --------------------
   {Patti}
```

<span data-ttu-id="3e7bb-109">O primeiro comando cria um objeto de detalhes do administrador de certificados e, em seguida, o armazena na variável $AdminDetails dados.</span><span class="sxs-lookup"><span data-stu-id="3e7bb-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>
<span data-ttu-id="3e7bb-110">O segundo comando cria um objeto de detalhes da organização de certificados e o armazena na variável $OrgDetails certificado.</span><span class="sxs-lookup"><span data-stu-id="3e7bb-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="3e7bb-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e7bb-111">PARAMETERS</span></span>

### <span data-ttu-id="3e7bb-112">-AdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="3e7bb-112">-AdministratorDetails</span></span>
<span data-ttu-id="3e7bb-113">Especifica os administradores da organização de certificados.</span><span class="sxs-lookup"><span data-stu-id="3e7bb-113">Specifies the certificate organization administrators.</span></span>

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

### <span data-ttu-id="3e7bb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e7bb-114">-DefaultProfile</span></span>
<span data-ttu-id="3e7bb-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="3e7bb-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e7bb-116">-ID</span><span class="sxs-lookup"><span data-stu-id="3e7bb-116">-Id</span></span>
<span data-ttu-id="3e7bb-117">Especifica o identificador da organização.</span><span class="sxs-lookup"><span data-stu-id="3e7bb-117">Specifies the identifier for the organization.</span></span>

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

### <span data-ttu-id="3e7bb-118">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3e7bb-118">-Confirm</span></span>
<span data-ttu-id="3e7bb-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e7bb-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e7bb-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e7bb-120">-WhatIf</span></span>
<span data-ttu-id="3e7bb-121">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3e7bb-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e7bb-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3e7bb-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e7bb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e7bb-123">CommonParameters</span></span>
<span data-ttu-id="3e7bb-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e7bb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e7bb-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e7bb-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e7bb-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="3e7bb-126">INPUTS</span></span>

### <span data-ttu-id="3e7bb-127">System.String</span><span class="sxs-lookup"><span data-stu-id="3e7bb-127">System.String</span></span>

### <span data-ttu-id="3e7bb-128">System.Collections.Generic.List'1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0,0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="3e7bb-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="3e7bb-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="3e7bb-129">OUTPUTS</span></span>

### <span data-ttu-id="3e7bb-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="3e7bb-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="3e7bb-131">Notas</span><span class="sxs-lookup"><span data-stu-id="3e7bb-131">NOTES</span></span>

## <span data-ttu-id="3e7bb-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3e7bb-132">RELATED LINKS</span></span>

[<span data-ttu-id="3e7bb-133">New-AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="3e7bb-133">New-AzKeyVaultCertificateAdministratorDetail</span></span>](./New-AzKeyVaultCertificateAdministratorDetail.md)

