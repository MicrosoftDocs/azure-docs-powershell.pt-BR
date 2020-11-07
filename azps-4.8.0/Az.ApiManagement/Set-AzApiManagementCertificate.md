---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
ms.openlocfilehash: 3c31da297b47c5d35c7d7b4eea5c55ca87d9521d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93956050"
---
# <span data-ttu-id="8abee-101">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="8abee-101">Set-AzApiManagementCertificate</span></span>

## <span data-ttu-id="8abee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8abee-102">SYNOPSIS</span></span>
<span data-ttu-id="8abee-103">Modifica um certificado de gerenciamento de API que está configurado para autenticação mútua com back-end.</span><span class="sxs-lookup"><span data-stu-id="8abee-103">Modifies an API Management certificate which is configured for mutual authentication with backend.</span></span>

## <span data-ttu-id="8abee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8abee-104">SYNTAX</span></span>

### <span data-ttu-id="8abee-105">LoadFromFile (padrão)</span><span class="sxs-lookup"><span data-stu-id="8abee-105">LoadFromFile (Default)</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxFilePath <String>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8abee-106">Brutas</span><span class="sxs-lookup"><span data-stu-id="8abee-106">Raw</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxBytes <Byte[]>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8abee-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8abee-107">DESCRIPTION</span></span>
<span data-ttu-id="8abee-108">O cmdlet **set-AzApiManagementCertificate** modifica um certificado de gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="8abee-108">The **Set-AzApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="8abee-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8abee-109">EXAMPLES</span></span>

### <span data-ttu-id="8abee-110">Exemplo 1: modificar um certificado</span><span class="sxs-lookup"><span data-stu-id="8abee-110">Example 1: Modify a certificate</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="8abee-111">Esse comando modifica o certificado de gerenciamento de API especificado.</span><span class="sxs-lookup"><span data-stu-id="8abee-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="8abee-112">OS</span><span class="sxs-lookup"><span data-stu-id="8abee-112">PARAMETERS</span></span>

### <span data-ttu-id="8abee-113">-Certificateid</span><span class="sxs-lookup"><span data-stu-id="8abee-113">-CertificateId</span></span>
<span data-ttu-id="8abee-114">Especifica a ID do certificado a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="8abee-114">Specifies the ID of the certificate to modify.</span></span>

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

### <span data-ttu-id="8abee-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="8abee-115">-Context</span></span>
<span data-ttu-id="8abee-116">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="8abee-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8abee-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8abee-117">-DefaultProfile</span></span>
<span data-ttu-id="8abee-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8abee-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8abee-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8abee-119">-PassThru</span></span>
<span data-ttu-id="8abee-120">PassThru</span><span class="sxs-lookup"><span data-stu-id="8abee-120">passthru</span></span>

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

### <span data-ttu-id="8abee-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="8abee-121">-PfxBytes</span></span>
<span data-ttu-id="8abee-122">Especifica uma matriz de bytes do arquivo de certificado no formato. pfx.</span><span class="sxs-lookup"><span data-stu-id="8abee-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="8abee-123">Esse parâmetro será necessário se você não especificar o parâmetro *PfxFilePath* .</span><span class="sxs-lookup"><span data-stu-id="8abee-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="8abee-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="8abee-124">-PfxFilePath</span></span>
<span data-ttu-id="8abee-125">Especifica o caminho para o arquivo de certificado no formato. pfx para criar e carregar.</span><span class="sxs-lookup"><span data-stu-id="8abee-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="8abee-126">Esse parâmetro será necessário se você não especificar o parâmetro *PfxBytes* .</span><span class="sxs-lookup"><span data-stu-id="8abee-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

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

### <span data-ttu-id="8abee-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="8abee-127">-PfxPassword</span></span>
<span data-ttu-id="8abee-128">Especifica a senha do certificado.</span><span class="sxs-lookup"><span data-stu-id="8abee-128">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="8abee-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8abee-129">CommonParameters</span></span>
<span data-ttu-id="8abee-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8abee-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8abee-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8abee-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8abee-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8abee-132">INPUTS</span></span>

### <span data-ttu-id="8abee-133">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8abee-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8abee-134">System. String</span><span class="sxs-lookup"><span data-stu-id="8abee-134">System.String</span></span>

### <span data-ttu-id="8abee-135">System. Byte []</span><span class="sxs-lookup"><span data-stu-id="8abee-135">System.Byte[]</span></span>

### <span data-ttu-id="8abee-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8abee-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8abee-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8abee-137">OUTPUTS</span></span>

### <span data-ttu-id="8abee-138">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="8abee-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="8abee-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8abee-139">NOTES</span></span>

## <span data-ttu-id="8abee-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8abee-140">RELATED LINKS</span></span>

[<span data-ttu-id="8abee-141">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="8abee-141">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="8abee-142">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="8abee-142">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="8abee-143">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="8abee-143">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)


