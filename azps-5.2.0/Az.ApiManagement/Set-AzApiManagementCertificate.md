---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
ms.openlocfilehash: 3c31da297b47c5d35c7d7b4eea5c55ca87d9521d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258609"
---
# <span data-ttu-id="d5c75-101">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="d5c75-101">Set-AzApiManagementCertificate</span></span>

## <span data-ttu-id="d5c75-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d5c75-102">SYNOPSIS</span></span>
<span data-ttu-id="d5c75-103">Modifica um certificado de gerenciamento de API que está configurado para autenticação mútua com back-end.</span><span class="sxs-lookup"><span data-stu-id="d5c75-103">Modifies an API Management certificate which is configured for mutual authentication with backend.</span></span>

## <span data-ttu-id="d5c75-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5c75-104">SYNTAX</span></span>

### <span data-ttu-id="d5c75-105">LoadFromFile (padrão)</span><span class="sxs-lookup"><span data-stu-id="d5c75-105">LoadFromFile (Default)</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxFilePath <String>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5c75-106">Brutas</span><span class="sxs-lookup"><span data-stu-id="d5c75-106">Raw</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxBytes <Byte[]>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5c75-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d5c75-107">DESCRIPTION</span></span>
<span data-ttu-id="d5c75-108">O cmdlet **set-AzApiManagementCertificate** modifica um certificado de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="d5c75-108">The **Set-AzApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="d5c75-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d5c75-109">EXAMPLES</span></span>

### <span data-ttu-id="d5c75-110">Exemplo 1: modificar um certificado</span><span class="sxs-lookup"><span data-stu-id="d5c75-110">Example 1: Modify a certificate</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="d5c75-111">Esse comando modifica o certificado de gerenciamento de API especificado.</span><span class="sxs-lookup"><span data-stu-id="d5c75-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="d5c75-112">OS</span><span class="sxs-lookup"><span data-stu-id="d5c75-112">PARAMETERS</span></span>

### <span data-ttu-id="d5c75-113">-Certificateid</span><span class="sxs-lookup"><span data-stu-id="d5c75-113">-CertificateId</span></span>
<span data-ttu-id="d5c75-114">Especifica a ID do certificado a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="d5c75-114">Specifies the ID of the certificate to modify.</span></span>

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

### <span data-ttu-id="d5c75-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="d5c75-115">-Context</span></span>
<span data-ttu-id="d5c75-116">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="d5c75-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d5c75-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5c75-117">-DefaultProfile</span></span>
<span data-ttu-id="d5c75-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d5c75-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5c75-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d5c75-119">-PassThru</span></span>
<span data-ttu-id="d5c75-120">PassThru</span><span class="sxs-lookup"><span data-stu-id="d5c75-120">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5c75-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="d5c75-121">-PfxBytes</span></span>
<span data-ttu-id="d5c75-122">Especifica uma matriz de bytes do arquivo de certificado no formato. pfx.</span><span class="sxs-lookup"><span data-stu-id="d5c75-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="d5c75-123">Esse parâmetro será necessário se você não especificar o parâmetro *PfxFilePath* .</span><span class="sxs-lookup"><span data-stu-id="d5c75-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="d5c75-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="d5c75-124">-PfxFilePath</span></span>
<span data-ttu-id="d5c75-125">Especifica o caminho para o arquivo de certificado no formato. pfx para criar e carregar.</span><span class="sxs-lookup"><span data-stu-id="d5c75-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="d5c75-126">Esse parâmetro será necessário se você não especificar o parâmetro *PfxBytes* .</span><span class="sxs-lookup"><span data-stu-id="d5c75-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

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

### <span data-ttu-id="d5c75-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="d5c75-127">-PfxPassword</span></span>
<span data-ttu-id="d5c75-128">Especifica a senha do certificado.</span><span class="sxs-lookup"><span data-stu-id="d5c75-128">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="d5c75-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5c75-129">CommonParameters</span></span>
<span data-ttu-id="d5c75-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5c75-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5c75-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5c75-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5c75-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d5c75-132">INPUTS</span></span>

### <span data-ttu-id="d5c75-133">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d5c75-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d5c75-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d5c75-134">System.String</span></span>

### <span data-ttu-id="d5c75-135">System. Byte []</span><span class="sxs-lookup"><span data-stu-id="d5c75-135">System.Byte[]</span></span>

### <span data-ttu-id="d5c75-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d5c75-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d5c75-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d5c75-137">OUTPUTS</span></span>

### <span data-ttu-id="d5c75-138">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="d5c75-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="d5c75-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d5c75-139">NOTES</span></span>

## <span data-ttu-id="d5c75-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d5c75-140">RELATED LINKS</span></span>

[<span data-ttu-id="d5c75-141">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="d5c75-141">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="d5c75-142">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="d5c75-142">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="d5c75-143">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="d5c75-143">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)


