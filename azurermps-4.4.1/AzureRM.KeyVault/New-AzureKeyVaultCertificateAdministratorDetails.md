---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificateAdministratorDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificateAdministratorDetails.md
ms.openlocfilehash: 28a2bb0c806fa152a742c2fc9e36b150116a6352
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427911"
---
# <span data-ttu-id="d027c-101">New-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="d027c-101">New-AzureKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="d027c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d027c-102">SYNOPSIS</span></span>
<span data-ttu-id="d027c-103">Cria um objeto de detalhes do administrador do certificado na memória.</span><span class="sxs-lookup"><span data-stu-id="d027c-103">Creates an in-memory certificate administrator details object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d027c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d027c-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificateAdministratorDetails [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d027c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d027c-105">DESCRIPTION</span></span>
<span data-ttu-id="d027c-106">O cmdlet **New-AzureKeyVaultCertificateAdministratorDetails** cria um objeto de detalhes do administrador do certificado na memória.</span><span class="sxs-lookup"><span data-stu-id="d027c-106">The **New-AzureKeyVaultCertificateAdministratorDetails** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="d027c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d027c-107">EXAMPLES</span></span>

### <span data-ttu-id="d027c-108">Exemplo 1: criar um objeto de detalhes do administrador do certificado</span><span class="sxs-lookup"><span data-stu-id="d027c-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\>$AdminDetails = New-AzureKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
```

<span data-ttu-id="d027c-109">Esse comando cria um objeto de detalhes do administrador do certificado na memória e, em seguida, armazena-o na variável $AdminDetails.</span><span class="sxs-lookup"><span data-stu-id="d027c-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="d027c-110">OS</span><span class="sxs-lookup"><span data-stu-id="d027c-110">PARAMETERS</span></span>

### <span data-ttu-id="d027c-111">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="d027c-111">-EmailAddress</span></span>
<span data-ttu-id="d027c-112">Especifica o endereço de email do administrador do certificado.</span><span class="sxs-lookup"><span data-stu-id="d027c-112">Specifies the email address for the certificate administrator.</span></span>

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

### <span data-ttu-id="d027c-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="d027c-113">-FirstName</span></span>
<span data-ttu-id="d027c-114">Especifica o primeiro nome do administrador do certificado.</span><span class="sxs-lookup"><span data-stu-id="d027c-114">Specifies the first name of the certificate administrator.</span></span>

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

### <span data-ttu-id="d027c-115">-LastName</span><span class="sxs-lookup"><span data-stu-id="d027c-115">-LastName</span></span>
<span data-ttu-id="d027c-116">Especifica o último nome do administrador do certificado.</span><span class="sxs-lookup"><span data-stu-id="d027c-116">Specifies the last name of the certificate administrator.</span></span>

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

### <span data-ttu-id="d027c-117">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="d027c-117">-PhoneNumber</span></span>
<span data-ttu-id="d027c-118">Especifica o número de telefone do administrador do certificado.</span><span class="sxs-lookup"><span data-stu-id="d027c-118">Specifies the phone number of the certificate administrator.</span></span>

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

### <span data-ttu-id="d027c-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d027c-119">-Confirm</span></span>
<span data-ttu-id="d027c-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d027c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d027c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d027c-121">-WhatIf</span></span>
<span data-ttu-id="d027c-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d027c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d027c-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d027c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d027c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d027c-124">-DefaultProfile</span></span>
<span data-ttu-id="d027c-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d027c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d027c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d027c-126">CommonParameters</span></span>
<span data-ttu-id="d027c-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d027c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d027c-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d027c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d027c-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d027c-129">INPUTS</span></span>

## <span data-ttu-id="d027c-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d027c-130">OUTPUTS</span></span>

### <span data-ttu-id="d027c-131">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="d027c-131">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="d027c-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d027c-132">NOTES</span></span>

## <span data-ttu-id="d027c-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d027c-133">RELATED LINKS</span></span>

[<span data-ttu-id="d027c-134">New-AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="d027c-134">New-AzureKeyVaultCertificateOrganizationDetails</span></span>](./New-AzureKeyVaultCertificateOrganizationDetails.md)

