---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/new-AzKeyvaultcertificateadministratordetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetails.md
ms.openlocfilehash: 6844a8f4858452a1ebf9df306d75e495603703aa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775788"
---
# <span data-ttu-id="fa4d1-101">New-AzKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="fa4d1-101">New-AzKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="fa4d1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fa4d1-102">SYNOPSIS</span></span>
<span data-ttu-id="fa4d1-103">Cria um objeto de detalhes do administrador do certificado na memória.</span><span class="sxs-lookup"><span data-stu-id="fa4d1-103">Creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="fa4d1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fa4d1-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateAdministratorDetails [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa4d1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fa4d1-105">DESCRIPTION</span></span>
<span data-ttu-id="fa4d1-106">O cmdlet **New-AzKeyVaultCertificateAdministratorDetails** cria um objeto de detalhes do administrador do certificado na memória.</span><span class="sxs-lookup"><span data-stu-id="fa4d1-106">The **New-AzKeyVaultCertificateAdministratorDetails** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="fa4d1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fa4d1-107">EXAMPLES</span></span>

### <span data-ttu-id="fa4d1-108">Exemplo 1: criar um objeto de detalhes do administrador do certificado</span><span class="sxs-lookup"><span data-stu-id="fa4d1-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\>$AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
```

<span data-ttu-id="fa4d1-109">Esse comando cria um objeto de detalhes do administrador do certificado na memória e, em seguida, armazena-o na variável $AdminDetails.</span><span class="sxs-lookup"><span data-stu-id="fa4d1-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="fa4d1-110">OS</span><span class="sxs-lookup"><span data-stu-id="fa4d1-110">PARAMETERS</span></span>

### <span data-ttu-id="fa4d1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa4d1-111">-DefaultProfile</span></span>
<span data-ttu-id="fa4d1-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="fa4d1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa4d1-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="fa4d1-113">-EmailAddress</span></span>
<span data-ttu-id="fa4d1-114">Especifica o endereço de email do administrador do certificado.</span><span class="sxs-lookup"><span data-stu-id="fa4d1-114">Specifies the email address for the certificate administrator.</span></span>

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

### <span data-ttu-id="fa4d1-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="fa4d1-115">-FirstName</span></span>
<span data-ttu-id="fa4d1-116">Especifica o primeiro nome do administrador do certificado.</span><span class="sxs-lookup"><span data-stu-id="fa4d1-116">Specifies the first name of the certificate administrator.</span></span>

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

### <span data-ttu-id="fa4d1-117">-LastName</span><span class="sxs-lookup"><span data-stu-id="fa4d1-117">-LastName</span></span>
<span data-ttu-id="fa4d1-118">Especifica o último nome do administrador do certificado.</span><span class="sxs-lookup"><span data-stu-id="fa4d1-118">Specifies the last name of the certificate administrator.</span></span>

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

### <span data-ttu-id="fa4d1-119">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="fa4d1-119">-PhoneNumber</span></span>
<span data-ttu-id="fa4d1-120">Especifica o número de telefone do administrador do certificado.</span><span class="sxs-lookup"><span data-stu-id="fa4d1-120">Specifies the phone number of the certificate administrator.</span></span>

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

### <span data-ttu-id="fa4d1-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fa4d1-121">-Confirm</span></span>
<span data-ttu-id="fa4d1-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa4d1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa4d1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa4d1-123">-WhatIf</span></span>
<span data-ttu-id="fa4d1-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fa4d1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa4d1-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fa4d1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa4d1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa4d1-126">CommonParameters</span></span>
<span data-ttu-id="fa4d1-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa4d1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa4d1-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa4d1-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa4d1-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fa4d1-129">INPUTS</span></span>

### <span data-ttu-id="fa4d1-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="fa4d1-130">None</span></span>
<span data-ttu-id="fa4d1-131">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="fa4d1-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fa4d1-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fa4d1-132">OUTPUTS</span></span>

### <span data-ttu-id="fa4d1-133">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="fa4d1-133">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="fa4d1-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fa4d1-134">NOTES</span></span>

## <span data-ttu-id="fa4d1-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fa4d1-135">RELATED LINKS</span></span>

[<span data-ttu-id="fa4d1-136">New-AzKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="fa4d1-136">New-AzKeyVaultCertificateOrganizationDetails</span></span>](./New-AzKeyVaultCertificateOrganizationDetails.md)

