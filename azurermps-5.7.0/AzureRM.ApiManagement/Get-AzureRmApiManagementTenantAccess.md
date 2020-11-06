---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantAccess.md
ms.openlocfilehash: 64f341398ff20f3eddf67c88c51a93125904d566
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429923"
---
# <span data-ttu-id="181b3-101">Get-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="181b3-101">Get-AzureRmApiManagementTenantAccess</span></span>

## <span data-ttu-id="181b3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="181b3-102">SYNOPSIS</span></span>
<span data-ttu-id="181b3-103">Obtém a configuração do Access para um locatário.</span><span class="sxs-lookup"><span data-stu-id="181b3-103">Gets the access configuration for a tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="181b3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="181b3-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantAccess -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="181b3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="181b3-105">DESCRIPTION</span></span>
<span data-ttu-id="181b3-106">O cmdlet **Get-AzureRmApiManagementTenantAccess** Obtém a configuração de acesso ao locatário para um locatário.</span><span class="sxs-lookup"><span data-stu-id="181b3-106">The **Get-AzureRmApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>

## <span data-ttu-id="181b3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="181b3-107">EXAMPLES</span></span>

### <span data-ttu-id="181b3-108">Exemplo 1: obter configuração de acesso ao locatário</span><span class="sxs-lookup"><span data-stu-id="181b3-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementTenantAccess -Context $apimContext 
```

<span data-ttu-id="181b3-109">Este comando obtém a configuração de acesso de locatário para o contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="181b3-109">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="181b3-110">OS</span><span class="sxs-lookup"><span data-stu-id="181b3-110">PARAMETERS</span></span>

### <span data-ttu-id="181b3-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="181b3-111">-Context</span></span>
<span data-ttu-id="181b3-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="181b3-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="181b3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="181b3-113">-DefaultProfile</span></span>
<span data-ttu-id="181b3-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="181b3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="181b3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="181b3-115">CommonParameters</span></span>
<span data-ttu-id="181b3-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="181b3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="181b3-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="181b3-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="181b3-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="181b3-118">INPUTS</span></span>

### <span data-ttu-id="181b3-119">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="181b3-119">None</span></span>
<span data-ttu-id="181b3-120">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="181b3-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="181b3-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="181b3-121">OUTPUTS</span></span>

### <span data-ttu-id="181b3-122">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="181b3-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="181b3-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="181b3-123">NOTES</span></span>

## <span data-ttu-id="181b3-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="181b3-124">RELATED LINKS</span></span>

[<span data-ttu-id="181b3-125">Set-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="181b3-125">Set-AzureRmApiManagementTenantAccess</span></span>](./Set-AzureRmApiManagementTenantAccess.md)


