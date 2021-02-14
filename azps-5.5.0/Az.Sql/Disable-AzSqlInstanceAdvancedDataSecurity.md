---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: 39b23c1b39121f143791667ade542080ba70ec95
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115767"
---
# <span data-ttu-id="265da-101">Disable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="265da-101">Disable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="265da-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="265da-102">SYNOPSIS</span></span>
<span data-ttu-id="265da-103">Desabilita a Segurança Avançada de Dados em uma instância gerenciada.</span><span class="sxs-lookup"><span data-stu-id="265da-103">Disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="265da-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="265da-104">SYNTAX</span></span>

```
Disable-AzSqlInstanceAdvancedDataSecurity [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="265da-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="265da-105">DESCRIPTION</span></span>
<span data-ttu-id="265da-106">O cmdlet **Disable-AzSqlInstanceAdvancedDataSecurity** desabilita a Segurança de Dados Avançada em uma instância gerenciada.</span><span class="sxs-lookup"><span data-stu-id="265da-106">The **Disable-AzSqlInstanceAdvancedDataSecurity** cmdlet disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="265da-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="265da-107">EXAMPLES</span></span>

### <span data-ttu-id="265da-108">Exemplo 1 - Desabilitar a segurança de dados avançada da instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="265da-108">Example 1 - Disable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

### <span data-ttu-id="265da-109">Exemplo 2 - Desabilitar a Segurança de Dados Avançada do servidor do recurso de instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="265da-109">Example 2 - Disable server Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Disable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

## <span data-ttu-id="265da-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="265da-110">PARAMETERS</span></span>

### <span data-ttu-id="265da-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="265da-111">-DefaultProfile</span></span>
<span data-ttu-id="265da-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="265da-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="265da-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="265da-113">-InputObject</span></span>
<span data-ttu-id="265da-114">O objeto de instância gerenciada a ser usado com a operação de política de Segurança de Dados Avançada</span><span class="sxs-lookup"><span data-stu-id="265da-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="265da-115">-NomedaE ocorrência</span><span class="sxs-lookup"><span data-stu-id="265da-115">-InstanceName</span></span>
<span data-ttu-id="265da-116">Nome da instância gerenciada do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="265da-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="265da-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="265da-117">-ResourceGroupName</span></span>
<span data-ttu-id="265da-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="265da-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="265da-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="265da-119">-Confirm</span></span>
<span data-ttu-id="265da-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="265da-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="265da-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="265da-121">-WhatIf</span></span>
<span data-ttu-id="265da-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="265da-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="265da-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="265da-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="265da-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="265da-124">CommonParameters</span></span>
<span data-ttu-id="265da-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="265da-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="265da-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="265da-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="265da-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="265da-127">INPUTS</span></span>

### <span data-ttu-id="265da-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="265da-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="265da-129">System.String</span><span class="sxs-lookup"><span data-stu-id="265da-129">System.String</span></span>

## <span data-ttu-id="265da-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="265da-130">OUTPUTS</span></span>

### <span data-ttu-id="265da-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="265da-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="265da-132">Notas</span><span class="sxs-lookup"><span data-stu-id="265da-132">NOTES</span></span>

## <span data-ttu-id="265da-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="265da-133">RELATED LINKS</span></span>
