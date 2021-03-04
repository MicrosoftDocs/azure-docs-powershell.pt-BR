---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
ms.openlocfilehash: bb60ce1fc2cb20a24d1b445cf4a3729bf26747ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887066"
---
# <span data-ttu-id="693e0-101">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="693e0-101">Set-AzApiManagementCertificate</span></span>

## <span data-ttu-id="693e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="693e0-102">SYNOPSIS</span></span>
<span data-ttu-id="693e0-103">Modifica um certificado de Gerenciamento de API configurado para autenticação mútua com back-end.</span><span class="sxs-lookup"><span data-stu-id="693e0-103">Modifies an API Management certificate which is configured for mutual authentication with backend.</span></span>

## <span data-ttu-id="693e0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="693e0-104">SYNTAX</span></span>

### <span data-ttu-id="693e0-105">LoadFromFile (Padrão)</span><span class="sxs-lookup"><span data-stu-id="693e0-105">LoadFromFile (Default)</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxFilePath <String>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="693e0-106">Raw</span><span class="sxs-lookup"><span data-stu-id="693e0-106">Raw</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxBytes <Byte[]>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="693e0-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="693e0-107">DESCRIPTION</span></span>
<span data-ttu-id="693e0-108">O cmdlet **Set-AzApiManagementCertificate** modifica um certificado de Gerenciamento de API do Azure.</span><span class="sxs-lookup"><span data-stu-id="693e0-108">The **Set-AzApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="693e0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="693e0-109">EXAMPLES</span></span>

### <span data-ttu-id="693e0-110">Exemplo 1: Modificar um certificado</span><span class="sxs-lookup"><span data-stu-id="693e0-110">Example 1: Modify a certificate</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="693e0-111">Este comando modifica o certificado de Gerenciamento de API especificado.</span><span class="sxs-lookup"><span data-stu-id="693e0-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="693e0-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="693e0-112">PARAMETERS</span></span>

### <span data-ttu-id="693e0-113">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="693e0-113">-CertificateId</span></span>
<span data-ttu-id="693e0-114">Especifica a ID do certificado a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="693e0-114">Specifies the ID of the certificate to modify.</span></span>

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

### <span data-ttu-id="693e0-115">-Context</span><span class="sxs-lookup"><span data-stu-id="693e0-115">-Context</span></span>
<span data-ttu-id="693e0-116">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="693e0-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="693e0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="693e0-117">-DefaultProfile</span></span>
<span data-ttu-id="693e0-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="693e0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="693e0-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="693e0-119">-PassThru</span></span>
<span data-ttu-id="693e0-120">passthru</span><span class="sxs-lookup"><span data-stu-id="693e0-120">passthru</span></span>

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

### <span data-ttu-id="693e0-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="693e0-121">-PfxBytes</span></span>
<span data-ttu-id="693e0-122">Especifica uma matriz de bytes do arquivo de certificado no formato .pfx.</span><span class="sxs-lookup"><span data-stu-id="693e0-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="693e0-123">Esse parâmetro será necessário se você não especificar o *parâmetro PfxFilePath.*</span><span class="sxs-lookup"><span data-stu-id="693e0-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="693e0-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="693e0-124">-PfxFilePath</span></span>
<span data-ttu-id="693e0-125">Especifica o caminho para o arquivo de certificado no formato .pfx para criar e carregar.</span><span class="sxs-lookup"><span data-stu-id="693e0-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="693e0-126">Esse parâmetro será necessário se você não especificar o *parâmetro PfxBytes.*</span><span class="sxs-lookup"><span data-stu-id="693e0-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

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

### <span data-ttu-id="693e0-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="693e0-127">-PfxPassword</span></span>
<span data-ttu-id="693e0-128">Especifica a senha do certificado.</span><span class="sxs-lookup"><span data-stu-id="693e0-128">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="693e0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="693e0-129">CommonParameters</span></span>
<span data-ttu-id="693e0-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="693e0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="693e0-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="693e0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="693e0-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="693e0-132">INPUTS</span></span>

### <span data-ttu-id="693e0-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="693e0-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="693e0-134">System.String</span><span class="sxs-lookup"><span data-stu-id="693e0-134">System.String</span></span>

### <span data-ttu-id="693e0-135">System.Byte[]</span><span class="sxs-lookup"><span data-stu-id="693e0-135">System.Byte[]</span></span>

### <span data-ttu-id="693e0-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="693e0-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="693e0-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="693e0-137">OUTPUTS</span></span>

### <span data-ttu-id="693e0-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="693e0-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="693e0-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="693e0-139">NOTES</span></span>

## <span data-ttu-id="693e0-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="693e0-140">RELATED LINKS</span></span>

[<span data-ttu-id="693e0-141">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="693e0-141">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="693e0-142">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="693e0-142">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="693e0-143">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="693e0-143">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)


