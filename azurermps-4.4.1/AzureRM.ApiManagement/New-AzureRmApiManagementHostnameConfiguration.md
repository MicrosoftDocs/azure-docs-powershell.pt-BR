---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D4C465CE-1B8A-4CFC-BAA8-21CC66B7D6D6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementHostnameConfiguration.md
ms.openlocfilehash: 1b34903f402f7e8d432d16087f1e32fc7b7da3e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431225"
---
# <span data-ttu-id="0d2c7-101">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="0d2c7-101">New-AzureRmApiManagementHostnameConfiguration</span></span>

## <span data-ttu-id="0d2c7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0d2c7-102">SYNOPSIS</span></span>
<span data-ttu-id="0d2c7-103">Cria uma instância de PsApiManagementHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0d2c7-103">Creates an instance of PsApiManagementHostnameConfiguration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d2c7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0d2c7-104">SYNTAX</span></span>

```
New-AzureRmApiManagementHostnameConfiguration -CertificateThumbprint <String> -Hostname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d2c7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0d2c7-105">DESCRIPTION</span></span>
<span data-ttu-id="0d2c7-106">O cmdlet **New-AzureRmApiManagementHostnameConfiguration** é um comando auxiliar que cria uma instância de **PsApiManagementHostnameConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="0d2c7-106">The **New-AzureRmApiManagementHostnameConfiguration** cmdlet is a helper command that creates an instance of **PsApiManagementHostnameConfiguration**.</span></span>
<span data-ttu-id="0d2c7-107">Esse comando é usado com o cmdlet Set-AzureRmApiManagementHostnames.</span><span class="sxs-lookup"><span data-stu-id="0d2c7-107">This command is used with the Set-AzureRmApiManagementHostnames cmdlet.</span></span>

## <span data-ttu-id="0d2c7-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0d2c7-108">EXAMPLES</span></span>

### <span data-ttu-id="0d2c7-109">Exemplo 1: criar e inicializar uma instância de PsApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="0d2c7-109">Example 1: Create and initialize an instance of PsApiManagementHostnameConfiguration</span></span>
```
PS C:\>New-AzureRmApiManagementHostnameConfiguration -Hostname "portal.contoso.com" -CertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C"
```

<span data-ttu-id="0d2c7-110">Esse comando cria e Inicializa uma instância de **PsApiManagementHostnameConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="0d2c7-110">This command creates and initializes an instance of **PsApiManagementHostnameConfiguration**.</span></span>

## <span data-ttu-id="0d2c7-111">OS</span><span class="sxs-lookup"><span data-stu-id="0d2c7-111">PARAMETERS</span></span>

### <span data-ttu-id="0d2c7-112">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="0d2c7-112">-CertificateThumbprint</span></span>
<span data-ttu-id="0d2c7-113">Especifica a impressão digital do certificado.</span><span class="sxs-lookup"><span data-stu-id="0d2c7-113">Specifies the certificate thumbprint.</span></span>
<span data-ttu-id="0d2c7-114">O certificado deve ser importado primeiro com o cmdlet Import-AzureRmApiManagementHostnameCertificate.</span><span class="sxs-lookup"><span data-stu-id="0d2c7-114">The certificate must be first imported with the Import-AzureRmApiManagementHostnameCertificate cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d2c7-115">-Hostname</span><span class="sxs-lookup"><span data-stu-id="0d2c7-115">-Hostname</span></span>
<span data-ttu-id="0d2c7-116">Especifica o nome de host personalizado para o qual esse cmdlet cria a instância **PsApiManagementHostnameConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="0d2c7-116">Specifies the custom host name for which this cmdlet creates the **PsApiManagementHostnameConfiguration** instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d2c7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d2c7-117">-DefaultProfile</span></span>
<span data-ttu-id="0d2c7-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0d2c7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d2c7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d2c7-119">CommonParameters</span></span>
<span data-ttu-id="0d2c7-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d2c7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d2c7-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d2c7-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d2c7-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0d2c7-122">INPUTS</span></span>

## <span data-ttu-id="0d2c7-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0d2c7-123">OUTPUTS</span></span>

### <span data-ttu-id="0d2c7-124">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="0d2c7-124">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration</span></span>

## <span data-ttu-id="0d2c7-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0d2c7-125">NOTES</span></span>

## <span data-ttu-id="0d2c7-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0d2c7-126">RELATED LINKS</span></span>

[<span data-ttu-id="0d2c7-127">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="0d2c7-127">Import-AzureRmApiManagementHostnameCertificate</span></span>](./Import-AzureRmApiManagementHostnameCertificate.md)

[<span data-ttu-id="0d2c7-128">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="0d2c7-128">Set-AzureRmApiManagementHostnames</span></span>](./Set-AzureRmApiManagementHostnames.md)


