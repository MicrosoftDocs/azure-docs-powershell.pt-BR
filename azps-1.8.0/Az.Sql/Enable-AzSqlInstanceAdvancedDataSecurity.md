---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: faf93387f068c6ee8e83653d31b96a1f3ecdef70
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599058"
---
# <span data-ttu-id="59622-101">Enable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="59622-101">Enable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="59622-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="59622-102">SYNOPSIS</span></span>
<span data-ttu-id="59622-103">Habilita a segurança avançada de dados em uma instância gerenciada.</span><span class="sxs-lookup"><span data-stu-id="59622-103">Enables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="59622-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59622-104">SYNTAX</span></span>

```
Enable-AzSqlInstanceAdvancedDataSecurity [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="59622-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="59622-105">DESCRIPTION</span></span>
<span data-ttu-id="59622-106">O cmdlet **Enable-AzSqlInstanceAdvancedDataSecurity** habilita a segurança avançada de dados em uma instância gerenciada.</span><span class="sxs-lookup"><span data-stu-id="59622-106">The **Enable-AzSqlInstanceAdvancedDataSecurity** cmdlet enables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="59622-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="59622-107">EXAMPLES</span></span>

### <span data-ttu-id="59622-108">Exemplo 1-habilitar a instância gerenciada segurança de dados avançada</span><span class="sxs-lookup"><span data-stu-id="59622-108">Example 1 - Enable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Enable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" 

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="59622-109">Exemplo 2-habilitar a instância gerenciada segurança de dados avançada do recurso do servidor</span><span class="sxs-lookup"><span data-stu-id="59622-109">Example 2 - Enable managed instance Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Enable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="59622-110">OS</span><span class="sxs-lookup"><span data-stu-id="59622-110">PARAMETERS</span></span>

### <span data-ttu-id="59622-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59622-111">-DefaultProfile</span></span>
<span data-ttu-id="59622-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="59622-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59622-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59622-113">-InputObject</span></span>
<span data-ttu-id="59622-114">O objeto de instância gerenciado a ser usado com a operação de política de segurança de dados avançada</span><span class="sxs-lookup"><span data-stu-id="59622-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="59622-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="59622-115">-InstanceName</span></span>
<span data-ttu-id="59622-116">Nome da instância gerenciada do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="59622-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="59622-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59622-117">-ResourceGroupName</span></span>
<span data-ttu-id="59622-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="59622-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="59622-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="59622-119">-Confirm</span></span>
<span data-ttu-id="59622-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59622-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59622-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59622-121">-WhatIf</span></span>
<span data-ttu-id="59622-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="59622-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59622-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="59622-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59622-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59622-124">CommonParameters</span></span>
<span data-ttu-id="59622-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59622-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59622-126">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59622-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59622-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="59622-127">INPUTS</span></span>

### <span data-ttu-id="59622-128">Microsoft. Azure. Commands. Sql. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="59622-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="59622-129">System. String</span><span class="sxs-lookup"><span data-stu-id="59622-129">System.String</span></span>

## <span data-ttu-id="59622-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="59622-130">OUTPUTS</span></span>

### <span data-ttu-id="59622-131">Microsoft. Azure. Commands. Sql. AdvancedThreatProtection. Model. ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="59622-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="59622-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="59622-132">NOTES</span></span>

## <span data-ttu-id="59622-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="59622-133">RELATED LINKS</span></span>
