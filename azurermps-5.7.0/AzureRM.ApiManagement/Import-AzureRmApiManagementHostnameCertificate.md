---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 98367100-4FFD-46F6-8974-603B32533626
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/import-azurermapimanagementhostnamecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementHostnameCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementHostnameCertificate.md
ms.openlocfilehash: 9c5f819a34ea0e394888e8156dad7a897d18167f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440534"
---
# <span data-ttu-id="be54f-101">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="be54f-101">Import-AzureRmApiManagementHostnameCertificate</span></span>

## <span data-ttu-id="be54f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="be54f-102">SYNOPSIS</span></span>
<span data-ttu-id="be54f-103">Importa um certificado em um formato PFX para um serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="be54f-103">Imports a certificate in a PFX format for an API Management Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be54f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="be54f-104">SYNTAX</span></span>

```
Import-AzureRmApiManagementHostnameCertificate -ResourceGroupName <String> -Name <String>
 -HostnameType <PsApiManagementHostnameType> -PfxPath <String> -PfxPassword <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be54f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="be54f-105">DESCRIPTION</span></span>
<span data-ttu-id="be54f-106">O cmdlet **Import-AzureRmApiManagementHostnameCertificate** importa um certificado em um formato PFX para um serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="be54f-106">The **Import-AzureRmApiManagementHostnameCertificate** cmdlet imports a certificate in a PFX format for an API Management Service.</span></span>
<span data-ttu-id="be54f-107">O certificado deve ser usado para a configuração de hostnames personalizada.</span><span class="sxs-lookup"><span data-stu-id="be54f-107">The certificate is to be used for custom hostnames configuration.</span></span>

## <span data-ttu-id="be54f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="be54f-108">EXAMPLES</span></span>

### <span data-ttu-id="be54f-109">Exemplo 1: importar um certificado de nome de host de gerenciamento de API</span><span class="sxs-lookup"><span data-stu-id="be54f-109">Example 1: Import a API Management hostname certificate</span></span>
```
PS C:\>Import-AzureRmApiManagementHostnameCertificate -Name "ContosoApi" -ResourceGroupName Contoso -HostnameType "Proxy" -PfxPath "C:\proxycert.pfx" -PfxPassword "CertSecret"
```

<span data-ttu-id="be54f-110">Esse comando importa um certificado para um nome de host personalizado de proxy.</span><span class="sxs-lookup"><span data-stu-id="be54f-110">This command imports a certificate for a proxy custom hostname.</span></span>

## <span data-ttu-id="be54f-111">OS</span><span class="sxs-lookup"><span data-stu-id="be54f-111">PARAMETERS</span></span>

### <span data-ttu-id="be54f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be54f-112">-DefaultProfile</span></span>
<span data-ttu-id="be54f-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="be54f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="be54f-114">-HostNameType</span><span class="sxs-lookup"><span data-stu-id="be54f-114">-HostnameType</span></span>
<span data-ttu-id="be54f-115">Especifica o tipo de nome de host para o qual esse cmdlet carrega o certificado.</span><span class="sxs-lookup"><span data-stu-id="be54f-115">Specifies the host name type that this cmdlet loads the certificate for.</span></span>

<span data-ttu-id="be54f-116">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="be54f-116">Valid values are:</span></span> 

- <span data-ttu-id="be54f-117">Proxy</span><span class="sxs-lookup"><span data-stu-id="be54f-117">Proxy</span></span>
- <span data-ttu-id="be54f-118">Portal</span><span class="sxs-lookup"><span data-stu-id="be54f-118">Portal</span></span>

```yaml
Type: PsApiManagementHostnameType
Parameter Sets: (All)
Aliases: 
Accepted values: Proxy, Portal

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be54f-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="be54f-119">-Name</span></span>
<span data-ttu-id="be54f-120">Especifica o nome da implantação de gerenciamento de API que este cmdlet importa.</span><span class="sxs-lookup"><span data-stu-id="be54f-120">Specifies the name of the API Management deployment that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be54f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="be54f-121">-PassThru</span></span>
<span data-ttu-id="be54f-122">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="be54f-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="be54f-123">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="be54f-123">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be54f-124">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="be54f-124">-PfxPassword</span></span>
<span data-ttu-id="be54f-125">Especifica a senha para o arquivo de certificado. pfx.</span><span class="sxs-lookup"><span data-stu-id="be54f-125">Specifies the password for the .pfx certificate file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be54f-126">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="be54f-126">-PfxPath</span></span>
<span data-ttu-id="be54f-127">Especifica o caminho para um arquivo de certificado. pfx.</span><span class="sxs-lookup"><span data-stu-id="be54f-127">Specifies the path to a .pfx certificate file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be54f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be54f-128">-ResourceGroupName</span></span>
<span data-ttu-id="be54f-129">Especifica o nome do grupo de recursos sob o qual existe a implantação de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="be54f-129">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be54f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be54f-130">CommonParameters</span></span>
<span data-ttu-id="be54f-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be54f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be54f-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be54f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be54f-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="be54f-133">INPUTS</span></span>

### <span data-ttu-id="be54f-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="be54f-134">None</span></span>
<span data-ttu-id="be54f-135">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="be54f-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="be54f-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="be54f-136">OUTPUTS</span></span>

### <span data-ttu-id="be54f-137">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="be54f-137">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameCertificate</span></span>

## <span data-ttu-id="be54f-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="be54f-138">NOTES</span></span>

## <span data-ttu-id="be54f-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="be54f-139">RELATED LINKS</span></span>

[<span data-ttu-id="be54f-140">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="be54f-140">New-AzureRmApiManagementHostnameConfiguration</span></span>](./New-AzureRmApiManagementHostnameConfiguration.md)

[<span data-ttu-id="be54f-141">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="be54f-141">Set-AzureRmApiManagementHostnames</span></span>](./Set-AzureRmApiManagementHostnames.md)

