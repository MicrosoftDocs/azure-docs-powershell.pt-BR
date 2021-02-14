---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CAA3E6A9-7E1A-4D57-A269-0B2D3D9C3BEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSqlServerExtension.md
ms.openlocfilehash: 7903e13abf7e924898910ad007eefcf6800dcc61
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115476"
---
# <span data-ttu-id="54110-101">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="54110-101">Get-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="54110-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="54110-102">SYNOPSIS</span></span>
<span data-ttu-id="54110-103">Obtém as configurações de uma extensão do SQL Server em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="54110-103">Gets the settings for a SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="54110-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="54110-104">SYNTAX</span></span>

```
Get-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54110-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="54110-105">DESCRIPTION</span></span>
<span data-ttu-id="54110-106">O cmdlet **Get-AzVMSqlServerExtension** obtém as configurações da infraestrutura do SQL Server como um agente de serviço (IaaS) em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="54110-106">The **Get-AzVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a virtual machine.</span></span>

## <span data-ttu-id="54110-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="54110-107">EXAMPLES</span></span>

### <span data-ttu-id="54110-108">Exemplo 1: Obter as configurações de uma extensão do SQL Server em uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="54110-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="54110-109">Esse comando obtém as configurações da extensão do SQL Server em uma máquina virtual chamada ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="54110-109">This command gets the settings of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

### <span data-ttu-id="54110-110">Exemplo 2: Obter as configurações usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="54110-110">Example 2: Get the settings by using the pipeline</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service08" -Name "ContosoVM22" | Get-AzVMSqlServerExtension
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="54110-111">Esse comando obtém a máquina virtual chamada ContosoVM22 no serviço Service08 usando o cmdlet Get-AzVM usuário.</span><span class="sxs-lookup"><span data-stu-id="54110-111">This command gets the virtual machine named ContosoVM22 on the service Service08 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="54110-112">O comando passa os resultados para o cmdlet atual usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="54110-112">The command passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="54110-113">O comando atual obtém as configurações do Sql Server IaaS Agent nessa máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="54110-113">The current command gets the settings of the SQL Server IaaS Agent on that virtual machine.</span></span>

### <span data-ttu-id="54110-114">Exemplo 3: Obter as configurações de uma versão específica do SQL Server</span><span class="sxs-lookup"><span data-stu-id="54110-114">Example 3: Get the settings of specific SQL Server version</span></span>
```
PS C:\> Get-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07" -Version "1.0"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="54110-115">Esse comando obtém as configurações da versão 1.0 da extensão do SQL Server em uma máquina virtual chamada ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="54110-115">This command gets the settings of version 1.0 of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

## <span data-ttu-id="54110-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="54110-116">PARAMETERS</span></span>

### <span data-ttu-id="54110-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54110-117">-DefaultProfile</span></span>
<span data-ttu-id="54110-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="54110-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54110-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="54110-119">-Name</span></span>
<span data-ttu-id="54110-120">Especifica o nome da extensão do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="54110-120">Specifies the name of the SQL Server the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54110-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54110-121">-ResourceGroupName</span></span>
<span data-ttu-id="54110-122">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="54110-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="54110-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="54110-123">-VMName</span></span>
<span data-ttu-id="54110-124">Especifica o nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="54110-124">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54110-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54110-125">CommonParameters</span></span>
<span data-ttu-id="54110-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54110-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54110-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54110-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54110-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="54110-128">INPUTS</span></span>

### <span data-ttu-id="54110-129">System.String</span><span class="sxs-lookup"><span data-stu-id="54110-129">System.String</span></span>

## <span data-ttu-id="54110-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="54110-130">OUTPUTS</span></span>

### <span data-ttu-id="54110-131">Microsoft.Azure.Commands.Compute.VirtualMachineSqlServerExtensionContext</span><span class="sxs-lookup"><span data-stu-id="54110-131">Microsoft.Azure.Commands.Compute.VirtualMachineSqlServerExtensionContext</span></span>

## <span data-ttu-id="54110-132">Notas</span><span class="sxs-lookup"><span data-stu-id="54110-132">NOTES</span></span>

## <span data-ttu-id="54110-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="54110-133">RELATED LINKS</span></span>

[<span data-ttu-id="54110-134">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="54110-134">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="54110-135">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="54110-135">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="54110-136">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="54110-136">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


