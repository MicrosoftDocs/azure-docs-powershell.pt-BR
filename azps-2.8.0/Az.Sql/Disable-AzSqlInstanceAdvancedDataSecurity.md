---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: a5aa9029e9d787311bb5b0c13b761c14f2b8bbca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773154"
---
# <span data-ttu-id="b482f-101">Disable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="b482f-101">Disable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="b482f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b482f-102">SYNOPSIS</span></span>
<span data-ttu-id="b482f-103">Desabilita a segurança avançada de dados em uma instância gerenciada.</span><span class="sxs-lookup"><span data-stu-id="b482f-103">Disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="b482f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b482f-104">SYNTAX</span></span>

```
Disable-AzSqlInstanceAdvancedDataSecurity [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b482f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b482f-105">DESCRIPTION</span></span>
<span data-ttu-id="b482f-106">O cmdlet **Disable-AzSqlInstanceAdvancedDataSecurity** desabilita a segurança avançada de dados em uma instância gerenciada.</span><span class="sxs-lookup"><span data-stu-id="b482f-106">The **Disable-AzSqlInstanceAdvancedDataSecurity** cmdlet disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="b482f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b482f-107">EXAMPLES</span></span>

### <span data-ttu-id="b482f-108">Exemplo 1-desativar a instância gerenciada segurança de dados avançada</span><span class="sxs-lookup"><span data-stu-id="b482f-108">Example 1 - Disable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

### <span data-ttu-id="b482f-109">Exemplo 2-desabilitar a segurança de dados avançados do servidor do recurso de instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="b482f-109">Example 2 - Disable server Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Disable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

## <span data-ttu-id="b482f-110">OS</span><span class="sxs-lookup"><span data-stu-id="b482f-110">PARAMETERS</span></span>

### <span data-ttu-id="b482f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b482f-111">-DefaultProfile</span></span>
<span data-ttu-id="b482f-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b482f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b482f-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b482f-113">-InputObject</span></span>
<span data-ttu-id="b482f-114">O objeto de instância gerenciado a ser usado com a operação de política de segurança de dados avançada</span><span class="sxs-lookup"><span data-stu-id="b482f-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="b482f-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="b482f-115">-InstanceName</span></span>
<span data-ttu-id="b482f-116">Nome da instância gerenciada do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="b482f-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="b482f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b482f-117">-ResourceGroupName</span></span>
<span data-ttu-id="b482f-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b482f-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="b482f-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b482f-119">-Confirm</span></span>
<span data-ttu-id="b482f-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b482f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b482f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b482f-121">-WhatIf</span></span>
<span data-ttu-id="b482f-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b482f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b482f-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b482f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b482f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b482f-124">CommonParameters</span></span>
<span data-ttu-id="b482f-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b482f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b482f-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b482f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b482f-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b482f-127">INPUTS</span></span>

### <span data-ttu-id="b482f-128">Microsoft. Azure. Commands. Sql. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="b482f-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="b482f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b482f-129">System.String</span></span>

## <span data-ttu-id="b482f-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b482f-130">OUTPUTS</span></span>

### <span data-ttu-id="b482f-131">Microsoft. Azure. Commands. Sql. AdvancedThreatProtection. Model. ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="b482f-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="b482f-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b482f-132">NOTES</span></span>

## <span data-ttu-id="b482f-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b482f-133">RELATED LINKS</span></span>