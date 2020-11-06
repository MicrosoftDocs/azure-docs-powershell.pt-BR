---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantGitAccess.md
ms.openlocfilehash: 69f643f4d2e66f0b5af61a6362e59386b2f79078
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440237"
---
# <span data-ttu-id="aac56-101">Get-AzureRmApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="aac56-101">Get-AzureRmApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="aac56-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aac56-102">SYNOPSIS</span></span>
<span data-ttu-id="aac56-103">Obtém a configuração de acesso ao git para um locatário.</span><span class="sxs-lookup"><span data-stu-id="aac56-103">Gets the Git access configuration for a tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aac56-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aac56-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantGitAccess -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aac56-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aac56-105">DESCRIPTION</span></span>
<span data-ttu-id="aac56-106">O cmdlet **Get-AzureRmApiManagementTenantGitAccess** Obtém a configuração de acesso ao git para um locatário.</span><span class="sxs-lookup"><span data-stu-id="aac56-106">The **Get-AzureRmApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="aac56-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aac56-107">EXAMPLES</span></span>

### <span data-ttu-id="aac56-108">Exemplo 1: obter configuração de acesso ao locatário</span><span class="sxs-lookup"><span data-stu-id="aac56-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>Get-AzureRmApiManagementTenantGitAccess -Context $ApimContext
```

<span data-ttu-id="aac56-109">Este comando obtém a configuração de acesso ao git para o contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="aac56-109">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="aac56-110">OS</span><span class="sxs-lookup"><span data-stu-id="aac56-110">PARAMETERS</span></span>

### <span data-ttu-id="aac56-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="aac56-111">-Context</span></span>
<span data-ttu-id="aac56-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="aac56-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aac56-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aac56-113">-DefaultProfile</span></span>
<span data-ttu-id="aac56-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aac56-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aac56-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aac56-115">CommonParameters</span></span>
<span data-ttu-id="aac56-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aac56-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aac56-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aac56-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aac56-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aac56-118">INPUTS</span></span>

## <span data-ttu-id="aac56-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aac56-119">OUTPUTS</span></span>

### <span data-ttu-id="aac56-120">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="aac56-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="aac56-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aac56-121">NOTES</span></span>

## <span data-ttu-id="aac56-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aac56-122">RELATED LINKS</span></span>

