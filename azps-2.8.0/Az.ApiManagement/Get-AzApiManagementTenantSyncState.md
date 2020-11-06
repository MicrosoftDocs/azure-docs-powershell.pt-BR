---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 288EF15B-FE5C-44AE-ABD5-2B92F408B9EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantsyncstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
ms.openlocfilehash: c8d3ff0d268c4a84269585af7e769b46af663f5c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598085"
---
# <span data-ttu-id="450e8-101">Get-AzApiManagementTenantSyncState</span><span class="sxs-lookup"><span data-stu-id="450e8-101">Get-AzApiManagementTenantSyncState</span></span>

## <span data-ttu-id="450e8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="450e8-102">SYNOPSIS</span></span>
<span data-ttu-id="450e8-103">Obtém o status da sincronização mais recente entre o banco de dados de configuração e o repositório do git.</span><span class="sxs-lookup"><span data-stu-id="450e8-103">Gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="450e8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="450e8-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantSyncState -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="450e8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="450e8-105">DESCRIPTION</span></span>
<span data-ttu-id="450e8-106">O cmdlet **Get-AzApiManagementTenantSyncState** Obtém o status da sincronização mais recente entre o banco de dados de configuração e o repositório do git.</span><span class="sxs-lookup"><span data-stu-id="450e8-106">The **Get-AzApiManagementTenantSyncState** cmdlet gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="450e8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="450e8-107">EXAMPLES</span></span>

### <span data-ttu-id="450e8-108">Exemplo 1: obter o status da sincronização mais recente</span><span class="sxs-lookup"><span data-stu-id="450e8-108">Example 1: Get the status of the most recent synchronization</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantSyncState -Context $apimContext
```

<span data-ttu-id="450e8-109">Esse comando obtém o status da sincronização mais recente entre o banco de dados de configuração e o repositório do git.</span><span class="sxs-lookup"><span data-stu-id="450e8-109">This command gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="450e8-110">OS</span><span class="sxs-lookup"><span data-stu-id="450e8-110">PARAMETERS</span></span>

### <span data-ttu-id="450e8-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="450e8-111">-Context</span></span>
<span data-ttu-id="450e8-112">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="450e8-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="450e8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="450e8-113">-DefaultProfile</span></span>
<span data-ttu-id="450e8-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="450e8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="450e8-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="450e8-115">CommonParameters</span></span>
<span data-ttu-id="450e8-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="450e8-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="450e8-117">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="450e8-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="450e8-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="450e8-118">INPUTS</span></span>

### <span data-ttu-id="450e8-119">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="450e8-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="450e8-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="450e8-120">OUTPUTS</span></span>

### <span data-ttu-id="450e8-121">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementTenantConfigurationSyncState</span><span class="sxs-lookup"><span data-stu-id="450e8-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementTenantConfigurationSyncState</span></span>

## <span data-ttu-id="450e8-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="450e8-122">NOTES</span></span>

## <span data-ttu-id="450e8-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="450e8-123">RELATED LINKS</span></span>
