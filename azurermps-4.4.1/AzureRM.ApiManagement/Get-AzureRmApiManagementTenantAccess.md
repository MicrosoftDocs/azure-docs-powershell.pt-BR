---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantAccess.md
ms.openlocfilehash: 30243ef1796e621d0898aae38e29ddb1dc7fd20b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440240"
---
# <span data-ttu-id="d6781-101">Get-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="d6781-101">Get-AzureRmApiManagementTenantAccess</span></span>

## <span data-ttu-id="d6781-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d6781-102">SYNOPSIS</span></span>
<span data-ttu-id="d6781-103">Obtém a configuração do Access para um locatário.</span><span class="sxs-lookup"><span data-stu-id="d6781-103">Gets the access configuration for a tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6781-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d6781-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantAccess -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6781-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d6781-105">DESCRIPTION</span></span>
<span data-ttu-id="d6781-106">O cmdlet **Get-AzureRmApiManagementTenantAccess** Obtém a configuração de acesso ao locatário para um locatário.</span><span class="sxs-lookup"><span data-stu-id="d6781-106">The **Get-AzureRmApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>

## <span data-ttu-id="d6781-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d6781-107">EXAMPLES</span></span>

### <span data-ttu-id="d6781-108">Exemplo 1: obter configuração de acesso ao locatário</span><span class="sxs-lookup"><span data-stu-id="d6781-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>Get-AzureRmApiManagementTenantAccess -Context $ApimContext
```

<span data-ttu-id="d6781-109">Este comando obtém a configuração de acesso de locatário para o contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="d6781-109">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="d6781-110">OS</span><span class="sxs-lookup"><span data-stu-id="d6781-110">PARAMETERS</span></span>

### <span data-ttu-id="d6781-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="d6781-111">-Context</span></span>
<span data-ttu-id="d6781-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="d6781-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d6781-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6781-113">-DefaultProfile</span></span>
<span data-ttu-id="d6781-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d6781-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6781-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6781-115">CommonParameters</span></span>
<span data-ttu-id="d6781-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6781-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6781-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6781-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6781-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d6781-118">INPUTS</span></span>

## <span data-ttu-id="d6781-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d6781-119">OUTPUTS</span></span>

### <span data-ttu-id="d6781-120">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="d6781-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="d6781-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d6781-121">NOTES</span></span>

## <span data-ttu-id="d6781-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d6781-122">RELATED LINKS</span></span>

[<span data-ttu-id="d6781-123">Set-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="d6781-123">Set-AzureRmApiManagementTenantAccess</span></span>](./Set-AzureRmApiManagementTenantAccess.md)


