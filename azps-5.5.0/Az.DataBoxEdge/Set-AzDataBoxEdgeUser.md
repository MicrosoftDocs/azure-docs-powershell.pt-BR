---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
ms.openlocfilehash: 9074de6f4e6ee02a1476c1112d870b45d5bf6ccf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115429"
---
# <span data-ttu-id="de3fb-101">Set-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="de3fb-101">Set-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="de3fb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de3fb-102">SYNOPSIS</span></span>
<span data-ttu-id="de3fb-103">Define uma nova senha para um usuário no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="de3fb-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="de3fb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="de3fb-104">SYNTAX</span></span>

### <span data-ttu-id="de3fb-105">SetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="de3fb-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de3fb-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="de3fb-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de3fb-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de3fb-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -InputObject <PSDataBoxEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de3fb-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="de3fb-108">DESCRIPTION</span></span>
<span data-ttu-id="de3fb-109">O cmdlet **Set-AzDataBoxEdgeUser** define uma nova senha para um usuário no dispositivo de Borda da Caixa de Dados.</span><span class="sxs-lookup"><span data-stu-id="de3fb-109">The **Set-AzDataBoxEdgeUser** cmdlet sets a new password for a user on the Data Box Edge device.</span></span>

## <span data-ttu-id="de3fb-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="de3fb-110">EXAMPLES</span></span>

### <span data-ttu-id="de3fb-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="de3fb-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="de3fb-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="de3fb-112">PARAMETERS</span></span>

### <span data-ttu-id="de3fb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de3fb-113">-AsJob</span></span>
<span data-ttu-id="de3fb-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="de3fb-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de3fb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de3fb-115">-DefaultProfile</span></span>
<span data-ttu-id="de3fb-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="de3fb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de3fb-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="de3fb-117">-DeviceName</span></span>
<span data-ttu-id="de3fb-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="de3fb-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de3fb-119">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="de3fb-119">-EncryptionKey</span></span>
<span data-ttu-id="de3fb-120">Chave de criptografia do dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="de3fb-120">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de3fb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de3fb-121">-InputObject</span></span>
<span data-ttu-id="de3fb-122">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="de3fb-122">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de3fb-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="de3fb-123">-Name</span></span>
<span data-ttu-id="de3fb-124">Username</span><span class="sxs-lookup"><span data-stu-id="de3fb-124">Username</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de3fb-125">-Senha</span><span class="sxs-lookup"><span data-stu-id="de3fb-125">-Password</span></span>
<span data-ttu-id="de3fb-126">Senha, fornecer como uma cadeia de caracteres segura</span><span class="sxs-lookup"><span data-stu-id="de3fb-126">Password, provide as a secure string</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de3fb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de3fb-127">-ResourceGroupName</span></span>
<span data-ttu-id="de3fb-128">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="de3fb-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de3fb-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de3fb-129">-ResourceId</span></span>
<span data-ttu-id="de3fb-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="de3fb-130">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de3fb-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="de3fb-131">-Confirm</span></span>
<span data-ttu-id="de3fb-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de3fb-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de3fb-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de3fb-133">-WhatIf</span></span>
<span data-ttu-id="de3fb-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="de3fb-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="de3fb-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="de3fb-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de3fb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de3fb-136">CommonParameters</span></span>
<span data-ttu-id="de3fb-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de3fb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de3fb-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="de3fb-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de3fb-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="de3fb-139">INPUTS</span></span>

### <span data-ttu-id="de3fb-140">Nenhum</span><span class="sxs-lookup"><span data-stu-id="de3fb-140">None</span></span>

## <span data-ttu-id="de3fb-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="de3fb-141">OUTPUTS</span></span>

### <span data-ttu-id="de3fb-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="de3fb-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="de3fb-143">Notas</span><span class="sxs-lookup"><span data-stu-id="de3fb-143">NOTES</span></span>

## <span data-ttu-id="de3fb-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de3fb-144">RELATED LINKS</span></span>
