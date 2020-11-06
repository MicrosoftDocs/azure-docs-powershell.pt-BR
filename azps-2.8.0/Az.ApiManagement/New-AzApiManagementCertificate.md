---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5CBEDFF8-C441-44CC-B011-5F5AAFA2E5C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCertificate.md
ms.openlocfilehash: e2f32bc5d05121411a109c1371b52b41843cfc56
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598054"
---
# <span data-ttu-id="582fc-101">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="582fc-101">New-AzApiManagementCertificate</span></span>

## <span data-ttu-id="582fc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="582fc-102">SYNOPSIS</span></span>
<span data-ttu-id="582fc-103">Cria um certificado de gerenciamento de API para ser usado durante a autenticação com back-end.</span><span class="sxs-lookup"><span data-stu-id="582fc-103">Creates an API Management certificate to be used during Authentication with Backend.</span></span>

## <span data-ttu-id="582fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="582fc-104">SYNTAX</span></span>

### <span data-ttu-id="582fc-105">LoadFromFile (padrão)</span><span class="sxs-lookup"><span data-stu-id="582fc-105">LoadFromFile (Default)</span></span>
```
New-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxFilePath <String> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="582fc-106">Brutas</span><span class="sxs-lookup"><span data-stu-id="582fc-106">Raw</span></span>
```
New-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>] -PfxBytes <Byte[]>
 -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="582fc-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="582fc-107">DESCRIPTION</span></span>
<span data-ttu-id="582fc-108">O cmdlet **New-AzApiManagementCertificate** cria um certificado de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="582fc-108">The **New-AzApiManagementCertificate** cmdlet creates an Azure API Management certificate.</span></span>

## <span data-ttu-id="582fc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="582fc-109">EXAMPLES</span></span>

### <span data-ttu-id="582fc-110">Exemplo 1: criar e carregar um certificado</span><span class="sxs-lookup"><span data-stu-id="582fc-110">Example 1: Create and upload a certificate</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementCertificate -Context $ApiMgmtContext -PfxFilePath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111"
```

<span data-ttu-id="582fc-111">Esse comando carrega um certificado para o gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="582fc-111">This command uploads a certificate to Api Management.</span></span> <span data-ttu-id="582fc-112">Esse certificado pode ser usado para autenticação mútua com back-end usando políticas.</span><span class="sxs-lookup"><span data-stu-id="582fc-112">This certificate can be used for mutual authentication with backend using policies.</span></span>

## <span data-ttu-id="582fc-113">OS</span><span class="sxs-lookup"><span data-stu-id="582fc-113">PARAMETERS</span></span>

### <span data-ttu-id="582fc-114">-Certificateid</span><span class="sxs-lookup"><span data-stu-id="582fc-114">-CertificateId</span></span>
<span data-ttu-id="582fc-115">Especifica a ID do certificado a ser criado.</span><span class="sxs-lookup"><span data-stu-id="582fc-115">Specifies the ID of the certificate to create.</span></span>
<span data-ttu-id="582fc-116">Se você não especificar esse parâmetro, uma ID será gerada para você.</span><span class="sxs-lookup"><span data-stu-id="582fc-116">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="582fc-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="582fc-117">-Context</span></span>
<span data-ttu-id="582fc-118">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="582fc-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="582fc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="582fc-119">-DefaultProfile</span></span>
<span data-ttu-id="582fc-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="582fc-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="582fc-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="582fc-121">-PfxBytes</span></span>
<span data-ttu-id="582fc-122">Especifica uma matriz de bytes do arquivo de certificado no formato. pfx.</span><span class="sxs-lookup"><span data-stu-id="582fc-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="582fc-123">Esse parâmetro será necessário se você não especificar o parâmetro *PfxFilePath* .</span><span class="sxs-lookup"><span data-stu-id="582fc-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: Raw
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="582fc-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="582fc-124">-PfxFilePath</span></span>
<span data-ttu-id="582fc-125">Especifica o caminho para o arquivo de certificado no formato. pfx para criar e carregar.</span><span class="sxs-lookup"><span data-stu-id="582fc-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="582fc-126">Esse parâmetro será necessário se você não especificar o parâmetro *PfxBytes* .</span><span class="sxs-lookup"><span data-stu-id="582fc-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="582fc-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="582fc-127">-PfxPassword</span></span>
<span data-ttu-id="582fc-128">Especifica a senha do certificado.</span><span class="sxs-lookup"><span data-stu-id="582fc-128">Specifies the password for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="582fc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="582fc-129">CommonParameters</span></span>
<span data-ttu-id="582fc-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="582fc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="582fc-131">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="582fc-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="582fc-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="582fc-132">INPUTS</span></span>

### <span data-ttu-id="582fc-133">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="582fc-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="582fc-134">System. String</span><span class="sxs-lookup"><span data-stu-id="582fc-134">System.String</span></span>

### <span data-ttu-id="582fc-135">System. Byte []</span><span class="sxs-lookup"><span data-stu-id="582fc-135">System.Byte[]</span></span>

## <span data-ttu-id="582fc-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="582fc-136">OUTPUTS</span></span>

### <span data-ttu-id="582fc-137">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="582fc-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="582fc-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="582fc-138">NOTES</span></span>

## <span data-ttu-id="582fc-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="582fc-139">RELATED LINKS</span></span>

[<span data-ttu-id="582fc-140">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="582fc-140">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="582fc-141">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="582fc-141">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)

[<span data-ttu-id="582fc-142">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="582fc-142">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


