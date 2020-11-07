---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
ms.openlocfilehash: d9b179ab65fa4d081fd0d065d08dab42f8aee810
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942852"
---
# <span data-ttu-id="9b225-101">Get-AzApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="9b225-101">Get-AzApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="9b225-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9b225-102">SYNOPSIS</span></span>
<span data-ttu-id="9b225-103">Obtém a configuração de acesso ao git para um locatário.</span><span class="sxs-lookup"><span data-stu-id="9b225-103">Gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="9b225-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9b225-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9b225-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9b225-105">DESCRIPTION</span></span>
<span data-ttu-id="9b225-106">O cmdlet **Get-AzApiManagementTenantGitAccess** Obtém a configuração de acesso ao git para um locatário.</span><span class="sxs-lookup"><span data-stu-id="9b225-106">The **Get-AzApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="9b225-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9b225-107">EXAMPLES</span></span>

### <span data-ttu-id="9b225-108">Exemplo 1: obter configuração de acesso ao locatário</span><span class="sxs-lookup"><span data-stu-id="9b225-108">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccess -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="9b225-109">Este comando obtém a configuração de acesso ao git para o contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="9b225-109">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="9b225-110">OS</span><span class="sxs-lookup"><span data-stu-id="9b225-110">PARAMETERS</span></span>

### <span data-ttu-id="9b225-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="9b225-111">-Context</span></span>
<span data-ttu-id="9b225-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="9b225-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9b225-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b225-113">-DefaultProfile</span></span>
<span data-ttu-id="9b225-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9b225-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b225-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b225-115">CommonParameters</span></span>
<span data-ttu-id="9b225-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b225-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b225-117">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b225-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b225-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9b225-118">INPUTS</span></span>

### <span data-ttu-id="9b225-119">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9b225-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="9b225-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9b225-120">OUTPUTS</span></span>

### <span data-ttu-id="9b225-121">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="9b225-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="9b225-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9b225-122">NOTES</span></span>

## <span data-ttu-id="9b225-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9b225-123">RELATED LINKS</span></span>
