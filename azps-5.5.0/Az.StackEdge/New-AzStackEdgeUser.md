---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeUser.md
ms.openlocfilehash: 244adfb2707d47cef56390ce0d707b9f51fe229b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113680"
---
# <span data-ttu-id="7754c-101">New-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="7754c-101">New-AzStackEdgeUser</span></span>

## <span data-ttu-id="7754c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7754c-102">SYNOPSIS</span></span>
<span data-ttu-id="7754c-103">Cria um novo usuário para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7754c-103">Creates a new user for the device.</span></span>

## <span data-ttu-id="7754c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7754c-104">SYNTAX</span></span>

```
New-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [[-Type] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7754c-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="7754c-105">DESCRIPTION</span></span>
<span data-ttu-id="7754c-106">O **cmdlet New-AzSt stackEdgeUser** cria um novo usuário para o dispositivo Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="7754c-106">The **New-AzStackEdgeUser** cmdlet creates a new user for the Stack Edge device.</span></span> <span data-ttu-id="7754c-107">Há suporte para a criação de apenas usuários `Share` do tipo.</span><span class="sxs-lookup"><span data-stu-id="7754c-107">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="7754c-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7754c-108">EXAMPLES</span></span>

### <span data-ttu-id="7754c-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7754c-109">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

```powershell
PS C:\> New-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key -Type Share
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

## <span data-ttu-id="7754c-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7754c-110">PARAMETERS</span></span>

### <span data-ttu-id="7754c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7754c-111">-AsJob</span></span>
<span data-ttu-id="7754c-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7754c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7754c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7754c-113">-DefaultProfile</span></span>
<span data-ttu-id="7754c-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7754c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7754c-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="7754c-115">-DeviceName</span></span>
<span data-ttu-id="7754c-116">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="7754c-116">Device Name</span></span>

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

### <span data-ttu-id="7754c-117">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="7754c-117">-EncryptionKey</span></span>
<span data-ttu-id="7754c-118">Chave de criptografia do dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="7754c-118">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="7754c-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="7754c-119">-Name</span></span>
<span data-ttu-id="7754c-120">Username</span><span class="sxs-lookup"><span data-stu-id="7754c-120">Username</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7754c-121">-Senha</span><span class="sxs-lookup"><span data-stu-id="7754c-121">-Password</span></span>
<span data-ttu-id="7754c-122">Senha, fornecer como uma cadeia de caracteres segura</span><span class="sxs-lookup"><span data-stu-id="7754c-122">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="7754c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7754c-123">-ResourceGroupName</span></span>
<span data-ttu-id="7754c-124">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="7754c-124">Resource Group Name</span></span>

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

### <span data-ttu-id="7754c-125">-Tipo</span><span class="sxs-lookup"><span data-stu-id="7754c-125">-Type</span></span>
<span data-ttu-id="7754c-126">Selecionar UserType</span><span class="sxs-lookup"><span data-stu-id="7754c-126">Select UserType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7754c-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="7754c-127">-Confirm</span></span>
<span data-ttu-id="7754c-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7754c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7754c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7754c-129">-WhatIf</span></span>
<span data-ttu-id="7754c-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="7754c-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7754c-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7754c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7754c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7754c-132">CommonParameters</span></span>
<span data-ttu-id="7754c-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7754c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7754c-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7754c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7754c-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="7754c-135">INPUTS</span></span>

### <span data-ttu-id="7754c-136">Nenhum</span><span class="sxs-lookup"><span data-stu-id="7754c-136">None</span></span>

## <span data-ttu-id="7754c-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="7754c-137">OUTPUTS</span></span>

### <span data-ttu-id="7754c-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSSt stackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="7754c-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="7754c-139">Notas</span><span class="sxs-lookup"><span data-stu-id="7754c-139">NOTES</span></span>

## <span data-ttu-id="7754c-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7754c-140">RELATED LINKS</span></span>
