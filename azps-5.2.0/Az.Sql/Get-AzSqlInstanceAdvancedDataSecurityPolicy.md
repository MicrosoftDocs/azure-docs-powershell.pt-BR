---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceadvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 8adb699375a1b53f20e6027f35772642c658928b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259909"
---
# <span data-ttu-id="b0fc0-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="b0fc0-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="b0fc0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b0fc0-102">SYNOPSIS</span></span>
<span data-ttu-id="b0fc0-103">Obtém a política de segurança de dados avançada de uma instância gerenciada.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-103">Gets Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="b0fc0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b0fc0-104">SYNTAX</span></span>

```
Get-AzSqlInstanceAdvancedDataSecurityPolicy [-InputObject <AzureSqlManagedInstanceModel>]
 -InstanceName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b0fc0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b0fc0-105">DESCRIPTION</span></span>
<span data-ttu-id="b0fc0-106">O cmdlet **Get-AzSqlInstanceAdvancedDataSecurityPolicy** recupera a política de segurança de dados avançada de uma instância gerenciada.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-106">The **Get-AzSqlInstanceAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="b0fc0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b0fc0-107">EXAMPLES</span></span>

### <span data-ttu-id="b0fc0-108">Exemplo 1: Obtém a instância gerenciada segurança avançada de dados</span><span class="sxs-lookup"><span data-stu-id="b0fc0-108">Example 1: Gets managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlInstanceAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="b0fc0-109">Exemplo 2: Obtém a instância gerenciada segurança avançada de dados do recurso instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="b0fc0-109">Example 2: Gets managed instance Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Get-AzSqlInstanceAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="b0fc0-110">OS</span><span class="sxs-lookup"><span data-stu-id="b0fc0-110">PARAMETERS</span></span>

### <span data-ttu-id="b0fc0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0fc0-111">-DefaultProfile</span></span>
<span data-ttu-id="b0fc0-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0fc0-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0fc0-113">-InputObject</span></span>
<span data-ttu-id="b0fc0-114">O objeto de instância gerenciado a ser usado com a operação de política de segurança de dados avançada</span><span class="sxs-lookup"><span data-stu-id="b0fc0-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0fc0-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="b0fc0-115">-InstanceName</span></span>
<span data-ttu-id="b0fc0-116">Nome da instância gerenciada do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="b0fc0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0fc0-117">-ResourceGroupName</span></span>
<span data-ttu-id="b0fc0-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0fc0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0fc0-119">CommonParameters</span></span>
<span data-ttu-id="b0fc0-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0fc0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0fc0-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0fc0-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0fc0-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b0fc0-122">INPUTS</span></span>

### <span data-ttu-id="b0fc0-123">Microsoft. Azure. Commands. Sql. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="b0fc0-123">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="b0fc0-124">System. String</span><span class="sxs-lookup"><span data-stu-id="b0fc0-124">System.String</span></span>

## <span data-ttu-id="b0fc0-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b0fc0-125">OUTPUTS</span></span>

### <span data-ttu-id="b0fc0-126">Microsoft. Azure. Commands. Sql. AdvancedThreatProtection. Model. ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="b0fc0-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="b0fc0-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b0fc0-127">NOTES</span></span>

## <span data-ttu-id="b0fc0-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b0fc0-128">RELATED LINKS</span></span>
